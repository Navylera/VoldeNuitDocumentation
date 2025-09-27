# Surface

namespace: [VoldeNuit.Framework.Drawing](/Drawing/Drawing.md)

```C#
public static class Surface
```

Surface class Contains methods to support [Surface](https://manual.gamemaker.io/lts/en/GameMaker_Language/GML_Reference/Drawing/Surfaces/Surfaces.htm).

>Note: Without this class, you can directly set [RenderTarget2D](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.RenderTarget2D.html) and draw Texture.

### Static Methods Alias

</br>

#### RenderTarget2D surface_create(int width, int height)

Creates new RenderTarget and returns it.

- Returns: RenderTarget2D

|Parameter|Type|Desc|
|---|---|---|
|width|int|width of the RenderTarget.|
|height|int|height of the RenderTarget.|

```C#
public static RenderTarget2D surface_create(int width, int height) {}
```

</br>

### RenderTarget2D surface_exists(RenderTarget2D surface)

Returns whether RenderTarget that passed as argument is exists.

- Returns: bool (Whether RenderTarget is exists.)

|Parameter|Type|Desc|
|---|---|---|
|surface|RenderTarget2D|Reference of RenderTarget.|

```C#
public static bool RenderTarget2D surface_exists(RenderTarget2D surface) {}
```

</br>

### surface_set_target(RenderTarget2D surface)

Sets new RenderTarget.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|surface|RenderTarget2D|Reference of RenderTarget.|

```C#
public static void surface_set_target(RenderTarget2D surface) {}
```

</br>

### surface_reset_target()

Resets RenderTarget.

- Returns: N/A

```C#
public static void surface_reset_target() {}
```

</br>

### draw_serface(RenderTarget2D surface, float x, float y)

Draws RenderTarget that passed as argument to Screen.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|surface|RenderTarget2D|Reference of RenderTarget.|
|x|float|x position to draw.|
|y|float|y position to draw.|

```C#
public static void draw_serface(RenderTarget2D surface, float x, float y) {}
```

</br>

### surface_free(RenderTarget2D surface)

Dispose RenderTarget that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|surface|RenderTarget2D|Reference of RenderTarget.|

```C#
public static void surface_free(RenderTarget2D surface) {}
```

</br>

### surface_clear(uint color)

Clear current RenderTarget by color that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|color|uint|Color to clear RenderTarget.|

```C#
public static void surface_clear(uint color) {}
```

</br></br>