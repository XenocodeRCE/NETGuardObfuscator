# Hide Call Protection

Another thing that might reveal your sensitive code and how your program works is the Call Flow Graph of your application.

 The Call Flow of your program allow the hacker to trace the program flow trough all the methods in the classes.

{% tabs %}
{% tab title="BEFORE" %}
```csharp
Match match = (Match)obj;
ListViewItem listViewItem = this.resultListView.Items.Add(match.ToString());
listViewItem.SubItems.Add(match.Index.ToString());
listViewItem.SubItems.Add(match.Length.ToString());
```
{% endtab %}

{% tab title="AFTER" %}
```csharp
Match match = (Match)enumerator.Current;
ListViewItem listViewItem = <Module>.ó\u00B2)\u00A5Ä(calli(System.Windows.Forms.ListView/ListViewItemCollection(), this.resultListView, <Module>.CrossAppDomainData[39]), <Module>.Ï\u0091\u00A5Hÿ(match));
<Module>.V\u000FèÌ\u00B7(calli(System.Windows.Forms.ListViewItem/ListViewSubItemCollection(), listViewItem, <Module>.CrossAppDomainData[44]), calli(System.Int32(), match, <Module>.CrossAppDomainData[45]).ToString());
<Module>.V\u000FèÌ\u00B7(calli(System.Windows.Forms.ListViewItem/ListViewSubItemCollection(), listViewItem, <Module>.CrossAppDomainData[44]), calli(System.Int32(), match, <Module>.CrossAppDomainData[46]).ToString());
```
{% endtab %}
{% endtabs %}

