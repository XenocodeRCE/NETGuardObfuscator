---
description: βeta members got access to beta features that are not available publicly.
---

# βeta features

{% hint style="success" %}
To gain access to the βeta membership you must fulfill certain conditions. Please contact us.
{% endhint %}

{% hint style="info" %}
βeta features might be unstable. Nonetheless if something goes wrong contact us.
{% endhint %}

{% page-ref page="native-string-protection.md" %}

{% page-ref page="native-msil-code-encryption.md" %}

{% page-ref page="native-anti-debug.md" %}

{% page-ref page="native-anti-tamper.md" %}

## How to exclude it ? 

Due to the nature of this security, the resulting code can have performance impact.

Please use the Obfuscation Attribute like in our exemple to prevent this security from being applied on non-sensitive part of your program.

```csharp
// RegExTester.Program
// Token: 0x0600002F RID: 47 RVA: 0x00003417 File Offset: 0x00002417
[STAThread]
[Obfuscation(Exclude = false, Feature = "-native")]
private static void Main()
{
	Application.EnableVisualStyles();
	Application.SetCompatibleTextRenderingDefault(false);
	Application.Run(new frmMain());
}
```

