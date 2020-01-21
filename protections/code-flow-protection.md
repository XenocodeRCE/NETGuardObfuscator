---
description: Split functions in blocks and obscure the way they are executed.
---

# Code Flow Protection

![](../.gitbook/assets/codeflow.png)

## Description

The goal of this protection is to "spaghettify " the code execution flow while keeping its original functionality. That means the code should execute the same original tasks and instructions while providing a numbers of new proxy flow within the method.

The new method flow is meant to prevent hackers from understanding the method flow with ease. NETGuard uses VirtualMachine-based obfuscation techniques to protect the code flow stack value.

## Code Example

{% tabs %}
{% tab title="BEFORE" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000033 RID: 51 RVA: 0x00003548 File Offset: 0x00002548
private void testButton_Click(object sender, EventArgs e)
{
    if (this.testButton.Text == "Test [F5]")
    {
        this.StartTest();
        return;
    }
    if (this.testButton.Text == "Stop [Esc]")
    {
        this.AbortTest();
    }
}
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000039 RID: 57 RVA: 0x000069D4 File Offset: 0x00004BD4
private void testButton_Click(object sender, EventArgs e)
{
    if (this.testButton.Text == "Test [F5]")
    {
        goto IL_20;
    }
    goto IL_F5;
    int num2;
    int num4;
    for (;;)
    {
        IL_2B:
        int num = num2;
        uint num3;
        switch ((num3 = (uint)((~(~num) * -1298256071 ^ 691573724) - 2137251886 + num4)) % 6u)
        {
        case 0u:
            goto IL_F5;
        case 2u:
            return;
        case 3u:
            goto IL_20;
        case 4u:
            this.StartTest();
            num2 = (int)(num3 ^ 548416123u ^ 507462520u);
            num4 = (int)Program.CALLCONV[62];
            continue;
        case 5u:
            this.AbortTest();
            num2 = (int)(num3 - 4138857096u ^ 1633831253u);
            num4 = (int)Program.CALLCONV[63];
            continue;
        }
        break;
    }
    return;
    IL_20:
    num4 = 1904912783;
    num2 = -826226997;
    goto IL_2B;
    IL_F5:
    num2 = ((!(this.testButton.Text == "Stop [Esc]")) ? -2143424651 : -1760466103);
    num4 = -1100246372;
    goto IL_2B;
}
```
{% endtab %}
{% endtabs %}

## Obfuscation Impacts

{% hint style="success" %}
**Targets : Methods and Functions**
{% endhint %}

{% hint style="success" %}
**Strength :** ⭐⭐⭐⭐
{% endhint %}

{% hint style="danger" %}
**Multi-threading tasks should be marked as excluded from the obfuscation process due to the nature of the protection that adds too much code to keep insane speed in multi-threading code.**
{% endhint %}

