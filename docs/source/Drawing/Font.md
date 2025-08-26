# Font

namespace: [VoldeNuit.Framework.Drawing](/Drawing/Drawing.md)

```C#
public class Font: IDisposable
```

Contains texture and data for drawing text.

### Properties

</br>

#### name

Contains name of font file. It can be only assigned once.

>Note: supported file extensions is .ttf.\
The default path is "[Configuration.CONTENT_PATH_LINUX](/Configuration.md#content-path-linux)+Font" on Linux, 
 "[Configuration.CONTENT_PATH_WINDOWS](/Configuration.md#content-path-windows)+Font" on Windows, 
 "[Configuration.CONTENT_PATH_UNIVERSAL](/Configuration.md#content-path-universal)+Font" on the others.

```C#
public string name { get; init; }
```

</br>

#### size_font

Contains size of font. It can be only assigned once.

```C#
public uint size_font { get; init; }
```

</br>

#### range

Contains range of font to make texture.

```C#
public string range { set; }
```

</br></br>

### Properties Alias

</br>

#### FontName

Alias of [name](name).

```C#
public string FontName { get; init; }
```

</br>

#### FontSize

Alias of [size_font](size-font).

```C#
public uint FontSize;
```

</br>

#### FontRange

Alias of [range](range).

```C#
public string FontRange { set; }
```

</br></br>
