# Sprite

namespace: [VoldeNuit.Framework.Drawing](/Drawing/Drawing.md)

```C#
public class Sprite
```

>Note: Sprite class is created when that Sprite is referenced for the first time,
 and texture file is loaded at the same time.
 If no value is assigned to [texture_path](texture-path), tracks file with the same name as the class name.\
supported filename extensions are [.xnb](https://docs.monogame.net/articles/getting_to_know/whatis/content_pipeline/) and .png.\
The default path is "[Configuration.CONTENT_PATH](/Configuration.md#content-path)+Sprite".

### Properties

</br>

#### embedded
Contains whether resource is embedded or not. The default value is false.

>Note: Embedded resources support only .png files.

```C#
public bool embedded = false;
```

</br>

#### texture_path
Contains path of texture file. The default value is null. It can be only assigned once.
 If no value is assigned, tracks files with the same name as the class name.

>Note: To use embedded resources, follow the format below.
>```C#
>
>public YourSprite() {
>
>    embedded = true;
>    
>    texture_path = yourAssembly.GetManifestResourceNames().First(n => n.EndsWith("SpriteName.png"));
>
>    // Set Properties...
>}
>```

```C#
public string? texture_path { get; init; } = null;
```

</br>

#### x
Contains x-offset of the Sprite. The default value is 0. It can be only assigned once.

```C#
public int x { get; init; }
```

</br>

#### y
Contains y-offset of the Sprite. The default value is 0. It can be only assigned once.

```C#
public int y { get; init; }
```

</br>

#### sprite_width
Contains width of the Sprite. The texture is sliced vertically by this value. It can be only assigned once.

```C#
public int sprite_width { get; init; }
```

</br>

#### sprite_height
Contains height of the Sprite. The texture is sliced horizontally by this value. It can be only assigned once.
 If not assigned, it returns height of the texture.

```C#
public int sprite_height { get; init; }
```

</br>

#### image_number
image_number is read-only value that contains number of the sub-images of the Sprite.

```C#
public int image_number { get; }
```

</br>

#### bbox
Contains collision area of the Sprite.

>Note: Boundbox ignores offset of Sprite; Starts from (0, 0).

```C#
public Rectangle? bbox;
```

</br>

#### precise
precise is read-only value that contains [bbox](bbox) is defined or not.

```C#
public bool precise { get; }
```

</br></br>

### Methods

</br>

#### +(Sprite sprite, Sprite subsprite)
Returns the original Sprite with the provided Sprite added.

>Note: To add Sprite, the following conditions must be met:
> - The values of [sprite_height](sprite-height) and texture.Height of the original Sprite must be the same.
> - The values of [sprite_height](sprite-height) and texture.Height of the Sprite to add must be the same.
> - Both Sprite must have the same [sprite_height](sprite-height) value.

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|
|subsprite|Sprite|Reference of Sprite to add.|

```C#
public static Sprite operator +(Sprite sprite, Sprite subsprite) {}
```

</br>

#### +(Sprite sprite, Texture2D texture)
Returns the original Sprite with the passed [Texture](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.Texture2D.html) added.

>Note: To add Texture, the following conditions must be met:
> - The values of [sprite_height](sprite-height) and texture.Height of the original Sprite must be the same.
> - The values of texture.Height of the original Sprite and Height of the Texture to add must be the same.

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|
|texture|Texture2D|Reference of Texture to add.|

```C#
public static Sprite operator +(Sprite sprite, Texture2D texture) {}
```

</br>

#### Copy(out Sprite destination)
Returns deep copy of Sprite to the argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|destination|Sprite|Reference of original Sprite.|

```C#
public void Copy(out Sprite destination) {}
```

</br></br>

### Static Methods

</br>

#### sprite_copy(Sprite sprite)
Returns deep copy of passed Sprite as argument.

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|

```C#
public static Sprite sprite_copy(Sprite sprite) {}
```

</br>

#### Sprite sprite_set_alpha_from_sprite(Sprite sprite, int sindex, Sprite grayscale, int gindex)

Returns new Sprite that modified alpha based on the grayscale Sprite.

>Note: For mor information, see <https://manual.gamemaker.io/lts/en/GameMaker_Language/GML_Reference/Asset_Management/Sprites/Sprite_Manipulation/sprite_set_alpha_from_sprite.htm>.

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|
|sindex|int|Subimage of Sprite to modify.|
|grayscale|Sprite|Reference of grayscale Sprite.|
|gindex|int|Subimage of grayscale.|

</br></br>

### Properties Alias

</br>

#### TexturePath
Alias of [texture_path](texture-path).

>Note: To use embedded resources, follow the format below.
>```C#
>
>public YourSprite() {
>
>    embedded = true;
>    
>    TexturePath = yourAssembly.GetManifestResourceNames().First(n => n.EndsWith("SpriteName.png"));
>
>    // Set Properties...
>}
>```

```C#
public string? TexturePath { get; init; } = null;
```

</br>

#### X
Alias of [x](x).

```C#
public int X;
```

</br>

#### Y
Alias of [y](y).

```C#
public int Y;
```

</br>

#### Width
Alias of [sprite_width](sprite-width).

```C#
public int Width;
```

</br>

#### Height
Alias of [sprite_height](sprite-height).

```C#
public int Height;
```

</br>

#### ImageNumber
Alias of [image_number](image-number).

```C#
public int ImageNumber;
```

</br>

#### BoundBox
Alias of [bbox](bbox).

```C#
public Rectangle? BoundBox;
```

</br>

#### Precise
Alias of [precise](precise).

```C#
public bool Precise;
```

</br></br>

### Static Methods Alias

</br>

#### CopySprite(Sprite sprite)
Alias of [sprite_copy(Sprite sprite)](sprite-copy-sprite-sprite).

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|

```C#
public static Sprite CopySprite(Sprite sprite) {}
```

</br>

#### Sprite SetAlphaFromSprite(Sprite sprite, int spriteImageIndex, Sprite grayScale, int grayScaleImageIndex)
Alias of [sprite_set_alpha_from_sprite(Sprite sprite, int sindex, Sprite grayscale, int gindex](sprite-set-alpha-from-sprite-sprite-sprite-int-sindex-sprite-grayscale-int-gindex).

- Returns: Sprite

|Parameter|Type|Desc|
|---|---|---|
|sprite|Sprite|Reference of original Sprite.|
|spriteImageIndex|int|Subimage of Sprite to modify.|
|grayScale|Sprite|Reference of grayscale Sprite.|
|grayScaleImageIndex|int|Subimage of grayscale.|

```C#
public static Sprite sprite_set_alpha_from_sprite(Sprite sprite, int sindex, Sprite grayscale, int gindex) {}
```

</br></br>