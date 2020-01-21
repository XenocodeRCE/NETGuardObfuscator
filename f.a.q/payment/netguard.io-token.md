# What is a 'token' ?

![](../../.gitbook/assets/icons8-sac-d-and-39-argent-64.png)

## All NETGuard pricing plans include a pay-per-use option that use Token as virtual currency

It means that you will **only pay for what you use**, you will not be charged monthly and pay for days when you want to obfuscate your file only once in a while.

`A token is a digital coin that you spare in order to unlock the premium statu, and therefore be able to select premium obfuscation techniques.`

That means **you can select as many obfuscation features as you want**, in the end you will always pay only one token per file.

Let's take an example with an imaginary program :

| Filename | MD5 | Token cost |
| :--- | :--- | :--- |
| myFile v1.0.0.0 | 4D1D4F2CF85A8F1DB9966B5196570ECB | 1 |
| myFile v1.0.0.0 | 4D1D4F2CF85A8F1DB9966B5196570ECB | 0 |
| myFile v1.0.0.0 | 4D1D4F2CF85A8F1DB9966B5196570ECB | 0 |
| myFile v1.0.0.1 | **D03EFD80B566869F7A526DC084B7E749** | 1 |
| myFile v1.0.0.0 | 4D1D4F2CF85A8F1DB9966B5196570ECB | 1 |

{% hint style="danger" %}
**Edited files, even only one byte, are considered to be different !**
{% endhint %}

As you can see, **if the last file you try to protect has its MD5 the same as the current file you want to obfuscate, the token cost is null**. That is meant to easily fix compatibility issue with strong obfuscation features.

However, **if you change / update the original file, its MD5 will change**, that is why **it will costs you a token**.

