---
description: Rename all of your functions and properties smartly.
---

# Name Protection

![](../.gitbook/assets/rename.png)

## Description

Names are what hackers and reverse engineer looks for when they want to trace your code in a decompiler and infer meaning of your methods. NETGuard.IO renaming pattern uses real names grabbed from .NET Framework library files to confuse them.

NETGuard.IO prevent the renaming of public members for library \(.dll\) files, while still renaming private and internal members. On executable \(.exe\) files NETGuard.IO apply a global renaming rules to rename every classes and methods in your project.

Names are also used a decoding key for specific back-ground algorithm, therefore if the file got passed in de4dot and gets renamed, it will not run anymore.

## Code Exemple

{% tabs %}
{% tab title="BEFORE" %}
```csharp
internal class LoginForm
{
    public LoginForm(Action<string, long, long, TimeSpan> statu)
    {
        this.SessionStatu= statu;
    }
    private Action<string, long, long, TimeSpan> Sessio;
}
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
internal class TypeInitializationException
{
    public TypeInitializationException(Action<string, long, long, TimeSpan> updateProgress)
    {
        this.DefaultDependencyAttribute = updateProgress;
    }
    private Action<string, long, long, TimeSpan> DefaultDependencyAttribute;
}
```
{% endtab %}
{% endtabs %}

## Obfuscation Impacts

{% hint style="success" %}
**Targets : Classes, Functions and Methods, Properties, Resources**
{% endhint %}

{% hint style="success" %}
**Strength :** ⭐⭐⭐⭐⭐
{% endhint %}

{% hint style="danger" %}
Make sure to mark JSON classes with the **\[Serialize\]** attribuute !
{% endhint %}

