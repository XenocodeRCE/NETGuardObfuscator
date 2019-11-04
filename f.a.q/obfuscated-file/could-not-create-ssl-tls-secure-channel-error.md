# "Could not create SSL/TLS secure channel" error

![](../../.gitbook/assets/icons8-recu-refuse-64.png)

{% hint style="warning" %}
This error can happen if you use a webClient to access an SSL/TLS secured endpoint.
{% endhint %}

Simply add this code to your method to remove the issue :

{% tabs %}
{% tab title="\[C\#\]" %}
```csharp
ServicePointManager.SecurityProtocol = SecurityProtocolType.Tls12;
```
{% endtab %}

{% tab title="\[VB.NET\]" %}
```fsharp
ServicePointManager.SecurityProtocol = SecurityProtocolType.Tls12
```
{% endtab %}
{% endtabs %}

