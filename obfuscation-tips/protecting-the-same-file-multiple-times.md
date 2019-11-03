# Updating my protected file ?

NETGuard will make you pay one token for each time the file is different from the last sent file.

That means, if you want to obfuscate `YourProgram.exe v1.0` it will costs you one token. If you want to obfuscate it again right after, since last sent file is equal to `YourProgram.exe v1.0` then it will not costs you a token.

However, if 2 hours ago you protected `YourProgram.exe v1.0` and now you want to protect `YourProgram.exe v2.0` then it will costs you a token because the file is a new file.

{% hint style="info" %}
We use **MD5** comparison to determine if files are equal or not.
{% endhint %}



