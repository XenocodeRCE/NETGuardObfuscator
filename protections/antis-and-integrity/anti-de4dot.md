# Anti De4Dot

NETGuard.IO injects invalid Type in your file to fool with De4Dot obfuscation detection engine. 

The saved file cannot run anymore because De4Dot removes code that looks useless but is not.

{% tabs %}
{% tab title="DE4DOT CONSOLE OUTPUT" %}
```coffeescript
de4dot v3.1.41592.3405 Copyright (C) 2011-2015 de4dot@gmail.com
Latest version and source code: https://github.com/0xd4d/de4dot

More than one obfuscator detected:
  Agile.NET (use: -p an)
  Babel .NET (use: -p bl)
  Crypto Obfuscator (use: -p co)
  Dotfuscator (use: -p df)
  Goliath.NET (use: -p go)
  SmartAssembly (use: -p sa)
  Spices.Net (use: -p sn)
  Xenocode (use: -p xc)
Detected Agile.NET (C:\file.exe)
Cleaning C:\file.exe
Renaming all obfuscated symbols
Saving C:\file.exe-cleaned.exe

C:\de4dot>
```
{% endtab %}
{% endtabs %}

