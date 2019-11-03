# Variable Melting Protection

Another scenario where numbers are sensitive data is memory editing : hackers modify value of integer variable in memory. 

To prevent that, NETGuard.IO turn integers into native IntPtr objects. The object's memory is now native and cannot be modified by external process.

{% tabs %}
{% tab title="BEFORE" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000037 RID: 55 RVA: 0x00003CA4 File Offset: 0x00002CA4
private void resultListView_SelectedIndexChanged(object sender, EventArgs e)
{
	if (this.resultListView.SelectedItems.Count == 0)
	{
		return;
	}
	this.textRichTextBox.Select(0, 0);
	int start = Convert.ToInt32(this.resultListView.SelectedItems[0].SubItems[1].Text);
	int length = Convert.ToInt32(this.resultListView.SelectedItems[0].SubItems[2].Text);
	this.textRichTextBox.Select(start, length);
}
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
// RegExTester.frmMain
// Token: 0x06000038 RID: 56 RVA: 0x00003DC8 File Offset: 0x00001FC8
private unsafe void resultListView_SelectedIndexChanged(object sender, EventArgs e)
{
	byte* ptr = stackalloc byte[(UIntPtr)8];
	if (this.resultListView.SelectedItems.Count == 0)
	{
		return;
	}
	this.textRichTextBox.Select(0, 0);
	int num = Convert.ToInt32(this.resultListView.SelectedItems[0].SubItems[1].Text);
	*(int*)ptr = num;
	int num2 = Convert.ToInt32(this.resultListView.SelectedItems[0].SubItems[2].Text);
	checked
	{
		*(int*)(ptr + 4) = num2;
		this.textRichTextBox.Select(*(int*)ptr, *(int*)(ptr + 4));
	}
}
```
{% endtab %}
{% endtabs %}

