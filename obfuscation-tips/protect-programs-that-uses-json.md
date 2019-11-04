---
description: How to correctly handle obfuscation on programs that uses JSON data
---

# Program that uses JSON data

JSON Data uses name of the property as **string**. That means when we rename the Methods and Classes in your assembly, NETGuard.IO will also rename the JSON Data and make it invalid. To prevent that, you must use the standard **\[Serializable\]** Attribute on the Class\(es\) that your program uses where the JSON data structure is implemented.

```csharp
[Serializable]
class jsonDATA
{
    public string username { get; set; }
    public string password { get; set; }
}
```

