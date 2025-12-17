# Color

namespace: [VoldeNuit.Framework.Drawing](/Drawing/Drawing.md)

Contains color for drawing.

>Note: VoldeNuit provides three ways to express color; ARGB, BGRA, and ABGR. The default is ARGB.\
>For more information, see [Configuration.COLOR_FORMAT](/Configuration.md#color-format).

```C#
public static class Color
```

### Static Properties

</br>

#### color
Contains color for drawing. The default value is 0xffffffffu. Primitives and Font following this color at that time.

```C#
public static uint color = 0xffffffffu;
```

</br>

#### A
Gets and sets A value.

```C#
public static byte A;
```

</br>

#### R
Gets and sets R value.

```C#
public static byte R;
```

</br>

#### R
Gets and sets G value.

```C#
public static byte G;
```

</br>

#### B
Gets and sets B value.

```C#
public static byte B;
```

</br></br>

### Static Methods

#### color_to_xna(uint color)

Returns the current [ColorFormat](/Configuration.md#color-format) as an [XNA Color object](https://docs.monogame.net/api/Microsoft.Xna.Framework.Color.html).

- Returns: [Microsoft.Xna.Framework.Color](https://docs.monogame.net/api/Microsoft.Xna.Framework.Color.html)

|Parameter|Type|Desc|
|---|---|---|
|color|uint|Color to convert.|

```C#
public static Microsoft.Xna.Framework.Color color_to_xna(uint color) {};
```

</br></br>

### Static Methods Alias

Alias of [color_to_xna(uint color)](color-to-xna-uint-color).

- Returns: [Microsoft.Xna.Framework.Color](https://docs.monogame.net/api/Microsoft.Xna.Framework.Color.html)

|Parameter|Type|Desc|
|---|---|---|
|color|uint|Color to convert.|

#### public static Microsoft.Xna.Framework.Color ColorToXna(uint color)

