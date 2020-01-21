---
description: MSIL code of each function is encrypted and decrypted at runtime.
---

# MSIL Code Encryption

![](../.gitbook/assets/msilencryption.png)

### Description <a id="description"></a>

Preventing hackers from accessing your code is our main priority. NETGuard.IO extract your method's MSIL instructions and encrypt them, the given data is injected into your file's header. The data is decoded at runtime when a checksum is validated. That means hackers and crackers doing static analysis won't be able to fetch your code.

{% hint style="warning" %}
This protection produces unverifiable modules.
{% endhint %}

{% hint style="success" %}
This protection serves an anti tampering purpose.
{% endhint %}

{% hint style="success" %}
This protection includes simple anti debugging checksum.
{% endhint %}

## Code example

{% tabs %}
{% tab title="BEFORE" %}
```csharp
// RegExTester.Program
// Token: 0x0600002F RID: 47 RVA: 0x00003417 File Offset: 0x00002417
[STAThread]
private static void Main()
{
    Application.EnableVisualStyles();
    Application.SetCompatibleTextRenderingDefault(false);
    Application.Run(new frmMain());
}
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
// RegExTester.Program
// Token: 0x0600002F RID: 47 RVA: 0x00003417 File Offset: 0x00002417
[STAThread]
private static void Main()
{
    /*
    An exception occurred when decompiling this method (0600000A)

    ICSharpCode.Decompiler.DecompilerException: Error decompiling System.Void _test.Program::.ctor()
     ---> System.ArgumentOutOfRangeException: Non-negative number required.
    Parameter name: length
       at System.Array.Copy(Array sourceArray, Int32 sourceIndex, Array destinationArray, Int32 destinationIndex, Int32 length, Boolean reliable)
       at System.Array.Copy(Array sourceArray, Array destinationArray, Int32 length)
       at ICSharpCode.Decompiler.ILAst.ILAstBuilder.StackSlot.ModifyStack(StackSlot[] stack, Int32 popCount, Int32 pushCount, ByteCode pushDefinition) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\ILAst\ILAstBuilder.cs:line 50
       at ICSharpCode.Decompiler.ILAst.ILAstBuilder.StackAnalysis(MethodDef methodDef) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\ILAst\ILAstBuilder.cs:line 373
       at ICSharpCode.Decompiler.ILAst.ILAstBuilder.Build(MethodDef methodDef, Boolean optimize, DecompilerContext context) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\ILAst\ILAstBuilder.cs:line 264
       at ICSharpCode.Decompiler.Ast.AstMethodBodyBuilder.CreateMethodBody(IEnumerable`1 parameters, MethodDebugInfoBuilder& builder) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\Ast\AstMethodBodyBuilder.cs:line 105
       at ICSharpCode.Decompiler.Ast.AstMethodBodyBuilder.CreateMethodBody(MethodDef methodDef, DecompilerContext context, IEnumerable`1 parameters, Boolean valueParameterIsKeyword, StringBuilder sb, MethodDebugInfoBuilder& stmtsBuilder) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\Ast\AstMethodBodyBuilder.cs:line 83
       --- End of inner exception stack trace ---
       at ICSharpCode.Decompiler.Ast.AstMethodBodyBuilder.CreateMethodBody(MethodDef methodDef, DecompilerContext context, IEnumerable`1 parameters, Boolean valueParameterIsKeyword, StringBuilder sb, MethodDebugInfoBuilder& stmtsBuilder) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\Ast\AstMethodBodyBuilder.cs:line 87
       at ICSharpCode.Decompiler.Ast.AstBuilder.CreateMethodBody(MethodDef method, IEnumerable`1 parameters, Boolean valueParameterIsKeyword, MethodKind methodKind, MethodDebugInfoBuilder& builder) in C:\projects\dnspy\Extensions\ILSpy.Decompiler\ICSharpCode.Decompiler\ICSharpCode.Decompiler\Ast\AstBuilder.cs:line 1358

    */;
}
```
{% endtab %}
{% endtabs %}

### Obfuscation Impacts

{% hint style="success" %}
**Targets : Assembly**
{% endhint %}

{% hint style="success" %}
**Strength :** ⭐⭐⭐⭐
{% endhint %}

{% hint style="danger" %}
**This protection produces unverifiable modules.**
{% endhint %}

