# Protect multi-threading tasks

Multi-threading task are meant to increase your file's task quickness, usually because your program relies on quickness to perform important task.

Obfuscation adds code to your file, and therefore the required time to perform your program's tasks is increased.

That is why you should always exclude method that contains multi-threading task from obfuscation.

{% hint style="danger" %}
Before doing so, make sure no sensitive data is in the same method, and if sensitive data is in the same method, put it in a separated method.
{% endhint %}

```csharp
[Obfuscation(Exclude = true)]
public void RunCheckCombolist()
{
    Stopwatch watch = new Stopwatch();
    watch.Start();
    Parallel.For(0, 100000, i =>
    {
        Thread.Sleep(1);
        counter++;
    });
    watch.Stop();
    Console.WriteLine("Seconds Elapsed: " + watch.Elapsed.Seconds);
    Console.WriteLine(counter.ToString());
    Console.ReadKey();
}
```

