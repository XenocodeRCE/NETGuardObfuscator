# "Could not create SSL/TLS secure channel" error

This error can happen if you use a webClient to access an SSL/TLS secured endpoint.

Add this code to your method to remove the issue :

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

