# Adding more security ?

## Rely on native packer / virtualization tools

Our obfuscator is strong, but no matter how strong it is, there is always a possibility for one to code a program to reverse the obfuscation process applied by NETGuard.IO on your file. With time and skills, one could almost completely remove the obfuscation layers of your file. That is why we try our best to fix managed software security issue : the fact that they are managed.

With the rise of dnlib, a library to modify managed files, more and more de-obfuscation tools have been created ; however they only target at MSIL level, that is managed. That is why we are doing our best to develop obfuscation techniques that not only rely on managed code but also on native techniques.

{% page-ref page="../protections/native-shield.md" %}

This protection produces a fresh native executable file from your managed executable file. Given the fact that you have now a native file, you are free to use any native packer / virtualization tools you want :

* VMProtect
* Themida
* X86 Virtualizer
* PELock 

Usage of native packer / virtualization tools can help to reduce the possibility of your program being cracked / de-obfuscated / unpacked.

{% hint style="warning" %}
If a compatibility issue happens when using their software, please contact them because only they can fix their respective software.
{% endhint %}

