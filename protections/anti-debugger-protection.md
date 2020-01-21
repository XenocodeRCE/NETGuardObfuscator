---
description: Prevents your file from running if a debugger is found on the machine.
---

# Anti Debug Protection

![](../.gitbook/assets/antidebug.png)

## Description

NETGuard.IO can prevent your file from being debugged by debugging tools and decompilers. We use WinAPI and managed techniques to prevent your file from being ran if a debugger is detected on the computer.

We automatically remove the file from the computer if a debugger is found in order to prevent any attempt at tampering your file.

## Obfuscation Impacts

{% hint style="success" %}
**Targets : Assembly**
{% endhint %}

{% hint style="success" %}
**Strenght :** ⭐⭐⭐⭐
{% endhint %}

{% hint style="warning" %}
**Startup time is a little bit longer due to the computer's file being scanned**
{% endhint %}

