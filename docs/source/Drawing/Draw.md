# Draw

namespace: [VoldeNuit.Framework.Drawing](/Drawing/Drawing.md)

```C#
public static class Draw
```

Contains methods for drawing.

>Note: Draw methods are executed only at Draw sequence(Begin_Draw, Draw, End_Draw and GUI_Draw).
>For more information, see [Heart.Draw()](/Heart.md#draw).

### Static Properties

</br>

#### halign

Contains text horizontal alignment. The default value is fa_left.

```C#
public static int halign = fa_left;

public const int fa_left   = 0;
public const int fa_center = 1;
public const int fa_right  = 2;
```

</br>

#### valign

Contains text vertical alignment. The default value is fa_top.

```C#
public static int halign = fa_left;

public const int fa_top    = 0;
public const int fa_middle = 1;
public const int fa_bottom = 2;
```

</br></br>

### Static Methods

</br>

#### draw_set_color(uint rgb)
Sets [color](./Color.md#color). Ignores alpha value.

|Parameter|Type|Desc|
|---|---|---|
|rgb|uint|Color to set.|

- Returns: N/A

```C#
public static void draw_set_color(uint rgb) {}
```

</br>

#### draw_set_alpha(float a)
Sets alpha of [color](./Color.md#color). Value ranges from 0 to 1.

|Parameter|Type|Desc|
|---|---|---|
|a|float|Alpha to set.|

- Returns: N/A

```C#
public static void draw_set_alpha(float a) {}
```

</br>

#### draw_line(float x1, float y1, float x2, float y2, int width = 1)
Draws line from (x1, y1) to (x2, y2). width must be greater than 1.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of start point.|
|y1|float|y position of start point.|
|x2|float|x position of end point.|
|y2|float|y position of end point.|
|width|int|Width of line.|

- Returns: N/A

```C#
public static void draw_line(float x1, float y1, float x2, float y2, int width = 1) {}
```

</br>

#### draw_rectangle(float x, float y, int width, int height, bool outline = false)
Draws rectangle.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position of rectangle.|
|y|float|y position of rectangle.|
|width|int|Width of rectangle.|
|height|int|Height of rectangle.|
|outline|bool|Whether the rectangle is drawn filled (false) or as a one pixel wide outline (true).|

```C#
public static void draw_rectangle(float x, float y, int width, int height, bool outline = false) {}
```

</br>

#### draw_sprite(Sprite sprite_index, float image_index, float x, float y)
Draws [Sprite](./Sprite.md).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sprite_index|Sprite|Reference of Sprite to draw.|
|image_index|float|Index of subimage.|
|x|float|x position of Sprite.|
|y|float|y position of Sprite.|

```C#
public static void draw_sprite(Sprite sprite_index, float image_index, float x, float y) {}
```

</br>

#### draw_sprite_ext(Sprite sprite_index, float image_index, float x, float y, float xscale, float yscale, float angle, uint color, float alpha)
Draws [Sprite](./Sprite.md) with additional options.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sprite_index|Sprite|Reference of Sprite to draw.|
|image_index|float|Index of subimage.|
|x|float|x position of Sprite.|
|y|float|y position of Sprite.|
|xscale|float|Xscale of Sprite.|
|yscale|float|Yscale of Sprite.|
|angle|float|Rotation of Sprite.|
|color|float|Color that blend to Sprite.|
|alpha|float|Alpha of Sprite.|

```C#
public static void draw_sprite_ext(Sprite sprite_index, float image_index, float x, float y, float xscale, float yscale, float angle, uint color, float alpha) {}
```

</br>

#### draw_sprite_part(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y)
Draws part of [Sprite](./Sprite.md).

>Note: This method ignores offset of Sprite ([Sprite.x](./Sprite.md#x) and [Sprite.y](./Sprite.md#y)).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sprite_index|Sprite|Reference of Sprite to draw.|
|image_index|float|Index of subimage.|
|left|int|x position on the Sprite of the left-top of the area to draw.|
|top|int|y position on the Sprite of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|

```C#
public static void draw_sprite_part(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y) {}
```

</br>

#### draw_sprite_part_ext(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha)
Draws part of [Sprite](./Sprite.md) with additional options.

>Note: This method ignores offset of Sprite ([Sprite.x](./Sprite.md#x) and [Sprite.y](./Sprite.md#y)).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sprite_index|Sprite|Reference of Sprite to draw.|
|image_index|float|Index of subimage.|
|left|int|x position on the Sprite of the left-top of the area to draw.|
|top|int|y position on the Sprite of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|
|xscale|float|Xscale of Sprite.|
|yscale|float|Yscale of Sprite.|
|color|float|Color that blend to Sprite.|
|alpha|float|Alpha of Sprite.|

```C#
public static void draw_sprite_part_ext(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha) {}
```

</br>

#### draw_set_font(Font font)
Sets default [Font](./Font.md).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|font|Font|Reference of Font to set.|

```C#
public static void draw_set_font(Font font) {}
```

</br>

#### draw_set_halign(int halign)
Sets [horizontal text alignment](halign).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|halign|[halign](halign)|Alignment constant to set.|

```C#
public static void draw_set_halign(int halign) {}
```

</br>

#### draw_set_valign(int valign)
Sets [vertical text alignment](valign).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|valign|[valign](valign)|Alignment constant to set.|

```C#
public static void draw_set_valign(int valign) {}
```

</br>

#### draw_text(float x, float y, string text, float xscale = 1f, float yscale = 1f, float angle = 0f)
Draws text.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to draw.|
|y|float|y position to draw.|
|text|string|Text to draw.|
|xscale|float|Xscale of texture. The default value is 1.|
|yscale|float|Yscale of texture. The default value is 1.|
|angle|float|Rotation of texture. The default value is 0.|

```C#
public static void draw_text(float x, float y, string text, float xscale = 1f, float yscale = 1f, float angle = 0f) {}
```

</br>

#### draw_text_ext(float x, float y, string text, float sep, float w, float xscale = 1f, float yscale = 1f, float angle = 0f)
Draws text with additional options.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to draw.|
|y|float|y position to draw.|
|text|string|Text to draw.|
|sep|float|Distance between lines of text.|
|w|float|Maximum width of the text before a line break.|
|xscale|float|Xscale of texture. The default value is 1.|
|yscale|float|Yscale of texture. The default value is 1.|
|angle|float|Rotation of texture. The default value is 0.|

```C#
public static void draw_text_ext(float x, float y, string text, float sep, float w, float xscale = 1f, float yscale = 1f, float angle = 0f) {}
```

</br>

#### string_width(string text)
Returns width of the text be drawn using the currently defined font.

- Returns: int (width of the text.)

|Parameter|Type|Desc|
|---|---|---|
|text|string|Text to measure.|

```C#
public static int string_width(string text) {}
```

</br>

#### draw_texture(Texture2D texture, float x, float y)
Draws [Texture](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.Texture2D.html).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|x|float|x position of Texture.|
|y|float|y position of Texture.|

```C#
public static void draw_texture(Texture2D texture, float x, float y) {}
```
</br>

#### draw_texture_ext(Texture2D texture, float x, float y, float xscale, float yscale, int vx, int vy, float angle, uint color, float alpha)
Draws [Texture](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.Texture2D.html) with additional options.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|x|float|x position of Texture.|
|y|float|y position of Texture.|
|xscale|float|Xscale of Texture.|
|yscale|float|Yscale of Texture.|
|vx|int|Xorigin of Texture.|
|vy|int|Yorigin of Texture.|
|angle|float|Rotation of Texture.|
|color|float|Color that blend to Texture.|
|alpha|float|Alpha of Texture.|

```C#
public static void draw_texture_ext(Texture2D texture, float x, float y, float xscale, float yscale, int vx, int vy, float angle, uint color, float alpha) {}
```

</br>

#### draw_texture_part(Texture2D texture, int left, int top, int width, int height, float x, float y)
Draws part of [Texture](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.Texture2D.html).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|left|int|x position on the Texture of the left-top of the area to draw.|
|top|int|y position on the Texture of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|

```C#
public static void draw_texture_part(Texture2D texture, int left, int top, int width, int height, float x, float y) {}
```

</br>

#### draw_texture_part_ext(Texture2D texture, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha)
Draws part of [Texture](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.Texture2D.html) with additional options.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|left|int|x position on the Texture of the left-top of the area to draw.|
|top|int|y position on the Texture of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|
|xscale|float|Xscale of Texture.|
|yscale|float|Yscale of Texture.|
|color|float|Color that blend to Texture.|
|alpha|float|Alpha of Texture.|

```C#
public static void draw_texture_part_ext(Texture2D texture, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha) {}
```

</br></br>

### Static Properties Alias

</br>

#### HorizontalAlign

Alias of [halign](halign).

```C#
public static int HorizontalAlign;

public const int HorizontalAlignLeft   = 0;
public const int HorizontalAlignCenter = 1;
public const int HorizontalAlignRight  = 2;
```

</br>

#### VerticalAlign

Alias of [valign](valign).

```C#
public static int VerticalAlign;

public const int VerticalAlignTop    = 3;
public const int VerticalAlignMiddle = 4;
public const int VerticalAlignBottom = 5;
```

</br></br>

### Static Methods Alias

</br>

#### SetDrawingColor(uint rgb)
Alias of [draw_set_color(uint rgb)](draw-set-color-uint-rgb).

|Parameter|Type|Desc|
|---|---|---|
|rgb|uint|Color to set.|

- Returns: N/A

```C#
public static void SetDrawingColor(uint rgb) {}
```

</br>

#### SetDrawingAlpha(float a)
Alias of [draw_set_alpha(float a)](draw-set-alpha-float-a).

|Parameter|Type|Desc|
|---|---|---|
|a|float|Alpha to set.|

- Returns: N/A

```C#
public static void SetDrawingAlpha(float a) {}
```

</br>

#### DrawLine(float x1, float y1, float x2, float y2, int width = 1)
Alias of [draw_line(float x1, float y1, float x2, float y2, int width = 1)](draw-line-float-x1-float-y1-float-x2-float-y2-int-width-1).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of start point.|
|y1|float|y position of start point.|
|x2|float|x position of end point.|
|y2|float|y position of end point.|
|width|int|Width of line.|

- Returns: N/A

```C#
public static void DrawLine(float x1, float y1, float x2, float y2, int width = 1) {}
```

</br>

#### DrawRectangle(float x, float y, int width, int height, bool outLine = false)
Alias of [draw_rectangle(float x, float y, int width, int height, bool outline = false)](draw-rectangle-float-x-float-y-int-width-int-height-bool-outline-false).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position of rectangle.|
|y|float|y position of rectangle.|
|width|int|Width of rectangle.|
|height|int|Height of rectangle.|
|outLine|bool|Whether the rectangle is drawn filled (false) or as a one pixel wide outline (true).|

```C#
public static void DrawRectangle(float x, float y, int width, int height, bool outLine = false) {}
```

</br>

#### DrawSprite(Sprite spriteIndex, float imageIndex, float x, float y)
Alias of [draw_sprite(Sprite sprite_index, float image_index, float x, float y)](draw-sprite-sprite-sprite-index-float-image-index-float-x-float-y).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|spriteIndex|Sprite|Reference of Sprite to draw.|
|imageIndex|float|Index of subimage.|
|x|float|x position of Sprite.|
|y|float|y position of Sprite.|

```C#
public static void DrawSprite(Sprite spriteIndex, float imageIndex, float x, float y) {}
```

</br>

#### DrawSprite(Sprite spriteIndex, float imageIndex, float x, float y, float xScale, float yScale, float angle, uint color, float alpha)
Alias of [draw_sprite_ext(Sprite sprite_index, float image_index, float x, float y, float xscale, float yscale, float angle, uint color, float alpha)](draw-sprite-ext-sprite-sprite-index-float-image-index-float-x-float-y-float-xscale-float-yscale-float-angle-uint-color-float-alpha).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|spriteIndex|Sprite|Reference of Sprite to draw.|
|imageIndex|float|Index of subimage.|
|x|float|x position of Sprite.|
|y|float|y position of Sprite.|
|xScale|float|Xscale of Sprite.|
|yScale|float|Yscale of Sprite.|
|angle|float|Rotation of Sprite.|
|color|float|Color that blend to Sprite.|
|alpha|float|Alpha of Sprite.|

```C#
public static void DrawSprite(Sprite spriteIndex, float imageIndex, float x, float y, float xScale, float yScale, float angle, uint color, float alpha) {}
```

</br>

#### DrawSpritePart(Sprite spriteIndex, float imageIndex, int left, int top, int width, int height, float x, float y)
Alias of [draw_sprite_part(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y)](draw-sprite-part-sprite-sprite-index-float-image-index-int-left-int-top-int-width-int-height-float-x-float-y).

>Note: This method ignores offset of Sprite ([Sprite.x](./Sprite.md#x) and [Sprite.y](./Sprite.md#y)).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|spriteIndex|Sprite|Reference of Sprite to draw.|
|imageIndex|float|Index of subimage.|
|left|int|x position on the Sprite of the left-top of the area to draw.|
|top|int|y position on the Sprite of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|

```C#
public static void DrawSpritePart(Sprite spriteIndex, float imageIndex, int left, int top, int width, int height, float x, float y) {}
```

</br>

#### DrawSpritePart(Sprite spriteIndex, float imageIndex, int left, int top, int width, int height, float x, float y, float xScale, float yScale, uint color, float alpha)
Alias of [draw_sprite_part_ext(Sprite sprite_index, float image_index, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha)](draw-sprite-part-ext-sprite-sprite-index-float-image-index-int-left-int-top-int-width-int-height-float-x-float-y-float-xscale-float-yscale-uint-color-float-alpha).

>Note: This method ignores offset of Sprite ([Sprite.x](./Sprite.md#x) and [Sprite.y](./Sprite.md#y)).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|spriteIndex|Sprite|Reference of Sprite to draw.|
|imageIndex|float|Index of subimage.|
|left|int|x position on the Sprite of the left-top of the area to draw.|
|top|int|y position on the Sprite of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|
|xScale|float|Xscale of Sprite.|
|yScale|float|Yscale of Sprite.|
|color|float|Color that blend to Sprite.|
|alpha|float|Alpha of Sprite.|

```C#
public static void DrawSpritePart(Sprite spriteIndex, float imageIndex, int left, int top, int width, int height, float x, float y, float xScale, float yScale, uint color, float alpha) {}
```

</br>

#### SetDrawingFont(Font font)
Alias of [draw_set_font(Font font)](draw-set-font-font-font).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|font|Font|Reference of Font to set.|

```C#
public void SetDrawingFont(Font font) {}
```

</br>

#### SetHorizontalAlign(int horizontalAlign)
Alias of [draw_set_halign(int halign)](draw-set-halign-int-halign).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|horizontalAlign|[HorizontalAlign](horizontalalign)|Alignment constant to set.|

```C#
public void SetHorizontalAlign(int horizontalAlign) {}
```

</br>

#### SetVerticalAlign(int verticalAlign)
Alias of [draw_set_valign(int valign)](draw-set-valign-int-valign).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|verticalAlign|[VerticalAlign](verticalalign)|Alignment constant to set.|

```C#
public void SetVerticalAlign(int verticalAlign) {}
```

</br>

#### DrawText(float x, float y, string text, float xScale = 1f, float yScale = 1f, float angle = 0f)
Alias of [draw_text(float x, float y, string text, float xscale = 1f, float yscale = 1f, float angle = 0f)](draw-text-float-x-float-y-string-text-float-xscale-1f-float-yscale-1f-float-angle-0f).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to draw.|
|y|float|y position to draw.|
|text|string|Text to draw.|
|xScale|float|Xscale of texture. The default value is 1.|
|yScale|float|Yscale of texture. The default value is 1.|
|angle|float|Rotation of texture. The default value is 0.|

```C#
public void DrawText(float x, float y, string text, float xScale = 1f, float yScale = 1f, float angle = 0f) {}
```

</br>

#### DrawText(float x, float y, string text, int lineBreakSpace, int maxWidth, float xScale = 1f, float yScale = 1f, float angle = 0f)
Alias of [draw_text_ext(float x, float y, string text, float sep, float w, float xscale = 1f, float yscale = 1f, float angle = 0f)](draw-text-ext-float-x-float-y-string-text-float-sep-float-w-float-xscale-1f-float-yscale-1f-float-angle-0f).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to draw.|
|y|float|y position to draw.|
|text|string|Text to draw.|
|lineBreakSpace|float|Distance between lines of text.|
|maxWidth|float|Maximum width of the text before a line break.|
|xScale|float|Xscale of texture. The default value is 1.|
|yScale|float|Yscale of texture. The default value is 1.|
|angle|float|Rotation of texture. The default value is 0.|

```C#
public void DrawText(float x, float y, string text, int lineBreakSpace, int maxWidth, float xScale = 1f, float yScale = 1f, float angle = 0f) {}
```

</br>


#### GetStringWidth(string text)
Alias of [string_width(string text)](string-width-string-text).

- Returns: int (width of the text.)

|Parameter|Type|Desc|
|---|---|---|
|text|string|Text to measure.|

```C#
public static int GetStringWidth(string text) {}
```

</br>

#### DrawTexture(Texture2D texture, float x, float y)
Alias of [draw_texure(Texture2D texture, float x, float y](draw-texture-texture2d-texture-float-x-float-y).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|x|float|x position of Texture.|
|y|float|y position of Texture.|

```C#
public static void DrawTexture(Texture2D texture, float x, float y) {}
```
</br>

#### DrawTexture(Texture2D texture, float x, float y, float xScale, float yScale, int vx, int vy, float angle, uint color, float alpha)
Alias of [draw_texture_ext(Texture2D texture, float x, float y, float xScale, float yScale, int vx, int vy, float angle, uint color, float alpha)](draw-texture-ext-texture2d-texture-float-x-float-y-float-xscale-float-yscale-int-vx-int-vy-float-angle-uint-color-float-alpha).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|x|float|x position of Texture.|
|y|float|y position of Texture.|
|xScale|float|Xscale of Texture.|
|yScale|float|Yscale of Texture.|
|vx|int|Xorigin of Texture.|
|vy|int|Yorigin of Texture.|
|angle|float|Rotation of Texture.|
|color|float|Color that blend to Texture.|
|alpha|float|Alpha of Texture.|

```C#
public static void DrawTexture(Texture2D texture, float x, float y, float xScale, float yScale, int vx, int vy, float angle, uint color, float alpha) {}
```

</br>

#### DrawTexturePart(Texture2D texture, int left, int top, int width, int height, float x, float y)
Alias of [draw_texture_part(Texture2D texture, int left, int top, int width, int height, float x, float y)](draw-texture-part-texture2d-texture-int-left-int-top-int-width-int-height-float-x-float-y).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|left|int|x position on the Texture of the left-top of the area to draw.|
|top|int|y position on the Texture of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|

```C#
public static void DrawTexturePart(Texture2D texture, int left, int top, int width, int height, float x, float y) {}
```

</br>

#### DrawTexturePart(Texture2D texture, int left, int top, int width, int height, float x, float y, float xScale, float yScale, uint color, float alpha)
Alias of [draw_texture_part_ext(Texture2D texture, int left, int top, int width, int height, float x, float y, float xscale, float yscale, uint color, float alpha)](draw-texture-part-ext-texture2d-texture-int-left-int-top-int-width-int-height-float-x-float-y-float-xscale-float-yscale-uint-color-float-alpha).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|texture|Texture2D|Reference of Texture to draw.|
|left|int|x position on the Texture of the left-top of the area to draw.|
|top|int|y position on the Texture of the left-top of the area to draw.|
|width|int|Width of the area to draw.|
|height|int|Height of the area to draw.|
|x|float|x position to draw area.|
|y|float|y position to draw area.|
|xScale|float|Xscale of Texture.|
|yScale|float|Yscale of Texture.|
|color|float|Color that blend to Texture.|
|alpha|float|Alpha of Texture.|

```C#
public static void DrawTexturePart(Texture2D texture, int left, int top, int width, int height, float x, float y, float xScale, float yScale, uint color, float alpha) {}
```
