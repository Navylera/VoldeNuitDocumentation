# Room

namespace: [VoldeNuit.Framework.Display](/Display/Display.md)

```C#
public class Room
```

Contains about [Camera](./Camera.md) and game room.

### Properties

</br>

#### camera
Contains [Camera](./Camera.md)s in the Room.

>Note: If no Camera is initialized when creating the [Room](./Room.md), Camera automatically created; Index is 0.

```C#
public readonly List<Camera> camera = [];
```

</br>

#### room_width
Contains width of the Room. The default value is 1 and the minimum value is 1.
```C#
public int room_width = 1;
```

</br>

#### room_height
Contains height of the Room. The default value is 1 and the minimum value is 1.
```C#
public int room_height = 1;
```

</br>

#### room_speed
Contains number of [Heart.Beat()](/Heart.md#beat) per second. The default value is 60.
```C#
public int room_speed = 60;
```

</br>

#### color_background
Contains color of background. The default value is 0xffffffff (255, 255, 255, 255).

>Note: VoldeNuit provides three ways to express color; ARGB, BGRA, and ABGR. The default is ARGB.\
>For more information, see [Configuration.COLOR_FORMAT](/Configuration.md#color-format).

```C#
public uint color_background = 0xffffffffu;
```

</br></br>

### Methods

</br>

#### Create()
Runs when Room is initialized.\

```C#
public virtual void Create() {}
```

>Note: Initialize properties of the Room here.\
 And by creating [Instance](/Instances/Instance.md)s in this method, you can place them in the Room.\
<br>
>e.g.
>
>```C#
>public override void Create() {
>
>    camera.Add(new Camera(0, 0, 640, 360, 0, 0, 1280, 720));
>
>    room_speed = 60;
>
>    background_color = 0xff000000u;
>
>    new Player() { x = 100, y = 100 };
>}
>```
>The code above initializes properties and create new Player on (100, 100).

</br></br>

### Static Methods

</br>

#### room_goto(Type name_room)
Initializes and Goes to Room passed as argument.

>Note: Even after this method has been executed, Instance runs the remaining code of the method.
 To prevent this, add return syntax after this method.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|name_room|Type|Type of Room to go.|

```C#
public static void room_goto(Type name_room) {}
```

</br></br>

### Properties Alias

</br>

#### Cameras
Alias of [camera](camera).

```C#
public readonly List<Camera> Cameras;
```

</br>

#### Width
Alias of [room_width](room-width).
```C#
public int Width;
```

</br>

#### Height
Alias of [room_height](room-height).
```C#
public int Height;
```

</br>

#### RoomSpeed
Alias of [room_speed](room-speed).
```C#
public int RoomSpeed;
```

</br>

#### BackgroundColor
Alias of [color_background](color-background).

```C#
public uint BackgroundColor;
```

</br></br>

### Static Methods Alias

</br>

#### GotoRoom(Type roomName)
Alias of [room_goto(Type name_room)](room-goto-type-name-room).
- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|name_room|Type|Type of Room to go.|

```C#
public static void GotoRoom(Type roomName) {}
```
