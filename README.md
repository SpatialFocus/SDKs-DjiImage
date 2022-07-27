# SDKs.DjiImage

## RJPEG
Dji thermal SDK Download Url： https://www.dji.com/cn/downloads/softwares/dji-thermal-sdk

```c#
byte[] data = System.IO.File.ReadAllBytes("1.JPG");
using (var img = RJPEG.FromBytes(data))
{
    AreaTemperature at = img.GetTempRect(0, 0, 100, 100);
    Console.WriteLine($"MinTemp={at.MinTemp} ,MaxTemp={at.MaxTemp}");
}
Console.ReadKey();
```