# Camera

namespace: [VoldeNuit.Framework.Display](/Display/Display.md)

```C#
public class Camera
```

Contains [View](./View.md) and [Viewport](./Viewport.md). The Viewport is drawn in index order.

>Note: If no Camera is initialized when creating the [Room](./Room.md), Camera automatically created; Index is 0.

### Properties

</br>

#### visible
Contains whether display on window or not. The default value is true.

```C#
public bool visible = true;
```

</br>

#### view
view is read-only value that contains the reference of the [View](./View.md).
```C#
public readonly View view;
```

</br>

#### viewport
viewport is read-only value that contains the reference of the [Viewport](./Viewport.md).
```C#
public readonly Viewport viewport;
```

</br>

#### colorfilter
Contains color mask value. The default value is 0xffffffff (255, 255, 255, 255).

>Note: VoldeNuit provides three ways to express color; ARGB, BGRA, and ABGR. The default is ARGB.\
>For more information, see [Configuration.COLOR_FORMAT](/Configuration.md#color-format).

```C#
public uint colorfilter = 0xffffffffu;
```

</br></br>

### Methods

</br>

#### Camera(int xview, int yview, int wview, int hview, int xport, int yport, int wport, int hport)
Constructor. Creates new Camera with properties and returns it.

- Returns: Camera

|Parameter|Type|Desc|
|---|---|---|
|xview|int|x position of View.|
|yview|int|y position of View.|
|wview|int|Width of View.|
|yview|int|Height of View.|
|xport|int|x position of Viewport.|
|yport|int|y position of Viewport.|
|wport|int|Width of Viewport.|
|yport|int|Height of Viewport.|

```C#
public Camera(int xview, int yview, int wview, int hview, int xport, int yport, int wport, int hport) {}
```

</br></br>

### Properties Alias

</br>

#### IsVisible
Alias of [visible](visible).

```C#
public bool IsVisible;
```

</br>

#### View
Alias of [view](view).
```C#
public readonly View View;
```

</br>

#### Viewport
Alias of [viewport](viewport).
```C#
public readonly Viewport Viewport;
```

</br>

#### ColorFilter
Alias of [colorfilter](colorfilter).
```C#
public uint ColorFilter;
```
