# Window

namespace: [VoldeNuit.Framework.Display](/Display/Display.md)

```C#
public static class Window
```

Contains methods to get game window properties.

### Static Properties

</br>

#### X
Gets and sets x position of game window.

```C#
public static int X;
```

</br>

#### Y
Gets and sets y position of game window.

```C#
public static int Y;
```

</br>

#### Width
Gets and sets width of game window.

- Returns: int

```C#
public static int Width;
```

</br>

#### Height
Gets and sets height of game window.

```C#
public static int Height;
```

</br></br>

### Static Methods

</br>

#### window_get_x()
Returns x position of game window.

- Returns: int

```C#
public static int window_get_x() {}
```

</br>

#### window_get_y()
Returns y position of game window.

- Returns: int

```C#
public static int window_get_y() {}
```

</br>

#### window_get_width()
Returns width of game window.

- Returns: int

```C#
public static int window_get_x() {}
```

</br>

#### window_get_height()
Returns width of game window.

- Returns: int

```C#
public static int window_get_x() {}
```

</br>

#### window_device()
Returns [GameWindow](https://docs.monogame.net/api/Microsoft.Xna.Framework.GameWindow.html).

- Returns: GameWindow

```C#
public static GameWindow window_device() {}
```

</br></br>

### Static Methods Alias

#### GetGameWindow()
Alias of [window_device()](window-device).

- Returns: GameWindow

```C#
public static GameWindow GetGameWindow() {}
```
