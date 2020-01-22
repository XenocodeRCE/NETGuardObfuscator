# Is my personal data safe ?

![](../../.gitbook/assets/icons8-appareil-photo-mural-prive-64.png)

## Privacy is the most important concern of the 21th century

Obfuscation and privacy both aim at allowing the target to be safe from mean people and abusers. In a way, obfuscating your file allow you to make your project code privacy higher than before.

Due to the fact that the Reverse Engineering scene has become something very toxic and harmful, while we obviously need to be present to watch what happens in the field of obfuscation, we decided to give ourselves some control over the usage of NETGuard Obfuscator; 

A few users with bad intentions were using our service to obfuscate target and then code some tools and scripts to try to automate the process of de-obfuscation. Some were also using our service to protect the source code of malware. 

{% hint style="success" %}
We do not allow illegal code to be protected using our service
{% endhint %}

To that extent, we decided to introduce some sort of detection engines within our obfuscation engines. It means that everytime you obfuscate a file, the server will produce a synthesis of different scans ran during the obfuscation process. This gather data on your file such as it's PE characteristics, it's MD5, it's date of creation, a neuronal network for discrimination analysis on your program's purpose, the name of your methods and classes and properties, the name of the external libraries your program uses, the discrimination analysis on the external libraries your program uses.

As you can see, we gather a lot of data, but keep in mind that to allow us to obfuscate your file, we do need complete access over the compiled binary, we will never ask you for the source code of your projects to make you obfuscate them. The obfuscation engines execute some \(de\)optimization routine and therefore needs read and write access to your program compiled file, and since c\# is not compiled to machine code but is compiled to MSIL, anyone can access the MSIL level with dnlib or mono.cecil libraries for instance.

The data we gather is exclusively used to make your user and customer experience better, we will never sell your data, we have been building a strong community since 2014 and we are proud to have this community even today. We offer you the chance to protect your source code against malicious users.

{% hint style="success" %}
We use strong encryption to protect all of your personal data on our servers.
{% endhint %}

