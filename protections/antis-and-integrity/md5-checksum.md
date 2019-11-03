# MD5 Checksum

NETGuard.IO prevent tampered obfuscated file from running by performing complex pre-calculations about your file's MD5 checksum and compare to its correct value  


```csharp
string location = Assembly.GetExecutingAssembly().Location;
Stream baseStream = new StreamReader(location).BaseStream;
BinaryReader binaryReader = new BinaryReader(baseStream);
string arg_5A_0 = BitConverter.ToString(MD5.Create().ComputeHash(binaryReader.ReadBytes(File.ReadAllBytes(location).Length - 16)));
baseStream.Seek(-16L, SeekOrigin.End);
string b = BitConverter.ToString(binaryReader.ReadBytes(16));
if (arg_5A_0 != b)
{
	throw new BadImageFormatException();
}
```



