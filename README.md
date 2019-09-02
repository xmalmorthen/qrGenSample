# qrGenSample

**Generador de QR de contenido extenso.**

### Librería

Nombre de espacio 
> **qrGenTool**

## Cómo usar

```c#
using qrGenTool;

...

qr.make( { cadena de texto } );

```

## Ejemplo [ Aplicación de consola ]
```c#
using System;
using System.Drawing;
using System.Drawing.Imaging;
using System.IO;
using qrGenTool;

namespace qrGenSample
{
    class Program
    {
        static void Main(string[] args)
        {
            string data = "";
            Image.FromStream(new MemoryStream(qr.make(data))).Save(Guid.NewGuid() + ".png", ImageFormat.Png);
        }
    }
}
```