---
description: Put sensitive data on our servers
---

# DRM Protection



![](../.gitbook/assets/cloud-development.png)

## Description

Your sensitive strings can be at risk if some malicious user wants to steal them by performing static or dynamic analysis of your file. **⛔**

With the DRM Protection, NETGuard.IO will encrypt your strings with a strong Advanced Encryption Standard algorithm, and the decoding key will be stored safely on our servers. **🚀** When launched, your obfuscated file will download the decoding key on our server's endpoint. The endpoint logs IP addresses of people that access it, this will allow us to offer you a white-list option in the near future **🍀**

Due to the nature of the protection, your file will always need internet access once DRM Protection is applied. Also if our servers goes down, even temporarily, your file will not be able to run properly \(we use a DDOS-protected hosting service to prevent that\).

{% hint style="danger" %}
This protection needs your file to access the internet to run properly .
{% endhint %}

{% hint style="success" %}
This protection logs IPs of whoever access your file, and prevents known hackers from doing anything harmfull to your code.
{% endhint %}

{% hint style="success" %}
This protection serves an anti-cracking purpose.
{% endhint %}

## Code exemple

{% tabs %}
{% tab title="BEFORE" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000033 RID: 51 RVA: 0x00002222 File Offset: 0x00000422
private void ignoreCaseButton_Click(object sender, EventArgs e)
{
	MessageBox.Show("This option makes the RegEx case-insensitive which means that 'a' and 'A' are treated as the same letter.", "Ignore Case Option", MessageBoxButtons.OK, MessageBoxIcon.Asterisk);
}
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000033 RID: 51 RVA: 0x000021C7 File Offset: 0x000003C7
private void ignoreCaseButton_Click(object sender, EventArgs e)
{
	MessageBox.Show(Koi.getKarp("HoPnc8iEHXZiG4yAYv7ub7E/irj4JucpI/NNYV5zC52B4wsVsWx6897F7ZJZ2oVyXQXHp5Htu6GlX7MVQSuASYDzz3lnmbTIGhwnDLieOb28DRnRawMJYpGNn1yaliGt3QMoXT6OFUUbu3DfnmTaDA=="), Koi.getKarp("aKNq8EST20T9rgy4gnKECEKIO7HsEgJbn6BAXN69ZBM="), MessageBoxButtons.OK, MessageBoxIcon.Asterisk);
}
```
{% endtab %}
{% endtabs %}

### Obfuscation Impacts

{% hint style="success" %}
**Targets : Methods**
{% endhint %}

{% hint style="success" %}
**Strength :** ⭐⭐⭐⭐
{% endhint %}

{% hint style="info" %}
**This protection's strength increases when selected with** [_**MSIL Coce Encryption**_](msil-code-encryption.md) **and** [_**Constants Protection**_](protections-of-constants.md)_\*\*\*\*_
{% endhint %}

