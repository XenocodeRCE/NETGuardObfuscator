---
description: >-
  VMProtect is a Native Virtualizer / Packer than can be used along with
  NETGuard.IO obfuscation using our Native Shield Protection feature.
---

# You also use VMProtect ?

{% embed url="https://www.youtube.com/watch?v=wZ9D0zkJRs0&feature=youtu.be" %}



If you select our **Native Shield Protection** you will be able to use every native packer / virtualizer on top of the file produced by NETGuard.IO obfuscation**.\***

{% page-ref page="../protections/file-shield/native-shield.md" %}

**NETGuard.IO** also comes with **Anti Dump Protection** to prevent your .NET Assembly from being dump by memory inspection tool, however with enough privilege on the kernel anyone could easily hook some APIs and dump the RAW bytes. 

{% page-ref page="../protections/antis-and-integrity/anti-dump.md" %}

To maximize the protection of your assembly, you can use [VMProtect ](https://vmpsoft.com/)and manually add the address of VirtualProtect to the Mutation/Virtualization queue. This is made in order to prevent hackers and crackers from finding the address of VirtualProtect, used to start the execution of the .NET Assembly from the Native stub.



