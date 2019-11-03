# Protections of Constants

## Strings

NETGuard offers to encode and encrypt string-based data. Strings are first encrypted using professional standard encryption algorithm to prevent any leak of data. The encryption part partially relies on x86 machine code generated method to prevent decompilers to retrieve the code logic.Then the newly created piece of code is encoded using state of the art obfuscation techniques to prevent anyone from understanding the code. The second step actually mutates the code into a meaningless code that makes the method safe from hackers.

{% tabs %}
{% tab title="BEFORE" %}
```csharp
this.contextStatusBarPanel.Text = string.Format("CLR {0}.{1}", Environment.Version.Major, Environment.Version.Minor);
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
string s = string.Format(<Module>.SuppressMessageAttribute<string>((uint)((6.0 * (double)num >= 10.0 + Math.Pow((double)num, 4.0) + (double)num * 6.0) ? ((int)((IntPtr)835599393)) : (-1774442645 - sizeof(ushort) - (int)Math.Floor(948.7677371109686))), (uint)((2.0 + Math.Sin((double)num2 * 1.0) >= 1.0) ? (-1401948064 - (int)Math.Floor(6649.3740176560232)) : ((int)((IntPtr)1008681497)))), NETGuardID, token);
```
{% endtab %}
{% endtabs %}

## Numbers

Numbers in your code can be very sensitive, and reveal a part of your keys. With that in mind, NETGuard uses the same logic we can find in string protection for integers and other numbers : x86 method encoding, strong encryption of actual value coupled with number decomposition.

{% tabs %}
{% tab title="BEFORE" %}
```csharp
int num = int.MinValue;
int num2 = int.MinValue;
int num3 = 0;
int num4 = 0;
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
uint num6 = (uint)((2.0 * (double)num5 >= 10.0 + Math.Pow((double)num5, 2.0) + (double)num5 * 2.0) ? 1900399322 : (-453298880 - Type.EmptyTypes.Length));
uint[] array3 = array;
array3[(10.0 + Math.Pow((double)num4, 2.0) + (double)num4 * 7.0 >= 7.0 * (double)num4) ? ((int)((IntPtr)Type.EmptyTypes.Length)) : 311978074] = (uint)((4.0 * (double)num >= 10.0 + Math.Pow((double)num, 4.0) + (double)num * 4.0) ? (168811203 - sizeof(DateTime) + (int)Math.Floor(317.15675077594665)) : -1485681892);
array3[(3.0 * (double)num >= 10.0 + Math.Pow((double)num, 4.0) + (double)num * 3.0) ? (1105999488 + (int)Math.Floor(9878.46086898421)) : (sizeof(<Module>.SafeCompressedStackHandle) + sizeof(byte) - sizeof(<Module>.SafeCompressedStackHandle))] = (uint)((6.0 >= 7.0 + Math.Sin((double)num2 * 2.0)) ? (218495996 + (int)Math.Floor(9878.4164446780542)) : (186488182 + Type.EmptyTypes.Length));
```
{% endtab %}
{% endtabs %}

