# README

![https://i.imgur.com/lajFbtv.png](https://i.imgur.com/lajFbtv.png)

## Presentation

NETGuard.IO is a **SaaS cloud-based obfuscator for files compiled for the Microsoft .NET Framework \(2.0-&gt;4.8\)** since 2014 ! Microsoft .NET compiled files are easily decompilable, it means that people can look at your source code and even modify it or exporting it to a new project source code, puting your source code at critical risks. **Obfuscation is one possible security layer you can use** combined with authentication system and piracy prevention system. Obfuscation will increase the entropy in your file in order to **complexify your source code while preserving the original tasks** performed by your file, **keepig hackers at bay** ! I usually take two very basic exemples :

* Take a puzzle, take apart its pieces slowly, and rebuild the puzzle. This is hackers playing with your file, easy peasy lemon sqeezy.
* Take that same puzzle, take apart its pieces, mix them up really hard randomly, cut some of them out, and try to rebuild the puzzle. This is hackers playing with your obfuscated file, significantly harder

## How it works

Microsoft .NET Framework compiled file follow the [ECMA standard](https://www.ecma-international.org/publications/standards/Ecma-335.htm), compiled into the Microsoft Intermediate Language MSIL, basically a scripting stack-based language. With high-end library such as [dnLib](https://github.com/0xd4d/dnlib) we are able to modify the MSIL representation of your source code directly on the compiled file, accessing the MSIL language operand in your file in a list format. **NETGuard.IO will modify this list content \(your compiled source code\) up to a point where the original task is executed but the list flow is not transparent and straightforward anymore.**

## Start using the obfuscator

Head over [NETGuard.IO official website](https://netguard.io) and sign up to use our service whenever you want ! There is a free plan with protection limitation, however if you report issues we will grant you some sort of compesation.

## Protection details / documentation

the wiki is currently being written, by some non-native english speakers :x

## Report an issue

Issues are bad, we hate them as much as you do. **Report and issue and we will grant you some sort of compensation.** To report an issue please go ahead to the [Issue](https://github.com/XenocodeRCE/NETGuardObfuscator/issues) page !

## Contact us

Please prefer the [Issue](https://github.com/XenocodeRCE/NETGuardObfuscator/issues) page for technical report.

Bonjour ! You can contact our tech support by sending a mail to **support@\[our domain including IO**\]. If mails are too old-fashioned for you, I also have Discord : `jusdepomme[hashtaaag typo is intended]60 twenty eight`. Speaking of discord, you can also **join this Obfuscator's Discord community** right [there](https://discord[dot%20gg]/YTTQSvG) \(be respectful\).

## Legal Notice

This is not an open-source project. Please read the [NotLicense](https://github.com/XenocodeRCE/NETGuardObfuscator/blob/master/NoLicense.md) notice.

