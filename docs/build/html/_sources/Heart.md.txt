# Heart

namespace: [VoldeNuit.Framework](/Framework.md)

```C#
public static class Heart
```

Heart class is static class that 
contains information about the overall game system and 
execute sequences.


### Static Properties

</br>

#### graphicsDevice

graphicsDevice is read-only value that contains reference of the current GraphicsDevice.

```C#
public static GraphicsDevice graphicsDevice { get; }
```

</br>

#### instance_id

Returns copy of list of current [Instances](/Instances/Instance.md) as read-only.

```C#
public static IList<Instance> instance_id;
```

</br>

#### instance_id_deactivated

Returns copy of list of current deactivated [Instances](/Instances/Instance.md) as read-only.

```C#
public static IList<Instance> instance_id_deactivated;
```

</br>

#### room_current

room_current is read-only value that contains reference of current [Room](/Display/Room.md).

```C#
public static Room room_current { get; }
```

</br>

#### room_width

Gets and sets width of current [Room](/Display/Room.md).

```C#
public static int room_width;
```

</br>

#### room_height

Gets and sets height of current [Room](/Display/Room.md).

```C#
public static int room_height;
```

</br>

#### room_speed

Gets and sets speed of current [Room](/Display/Room.md).

```C#
public static int room_speed;
```

</br>

#### instance_number

Returns number of [Instance](/Instances/Instance.md)s in current [Room](/Display/Room.md).

```C#
public static int instance_number { get; }
```

</br>

#### instance_number

Returns reference of current [Font](/Drawing/Font.md).

```C#
public static Font font_current { get; set; }
```

</br></br>

### Static Methods

</br>

#### InitMonoGameEnvironment(string projectName, Game game, GraphicsDeviceManager gDeviceManager)

Initializes environment values.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|projectname|string|name of the current project.|
|game|Game|Reference of [Game](https://docs.monogame.net/api/Microsoft.Xna.Framework.Game.html).|
|gDeviceManager|GraphicsDeviceManager|Reference of [GraphicsDeviceManager](https://docs.monogame.net/api/Microsoft.Xna.Framework.GraphicsDeviceManager.html).|

```C#
public static void InitMonoGameEnvironment(string projectName, Game game, GraphicsDeviceManager gdevicemanager) {}
```

</br>

#### InitResolution(int width, int height)

Initializes window resolution on game starts.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|width|int|Width of window.|
|height|int|Height of window.|

```C#
public static void InitResolution(int width, int height) {}
```

</br>

#### InitEntryPoint(Type room)

Initializes the [Room](/Display/Room.md) to enter when loading is finished.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|room|Type|Type of Room to enter.|

```C#
public static void InitEntryPoint(Type room) {}
```

</br>

#### InitSpriteBatch(SpriteBatch spriteBatch)

Initializes [SpriteBatch](https://docs.monogame.net/api/Microsoft.Xna.Framework.Graphics.SpriteBatch.html).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|spriteBatch|SpriteBatch|Reference of SpriteBatch.|

```C#
public static void InitSpriteBatch(SpriteBatch spriteBatch) {}
```

</br>

#### Beat()

Updates state of the game.

> The order of the event is as follows:
> Begin_Step -> Step -> End_Step
> 
> After the corresponding event for all Instances ends, the next event is executed.
> e.g. A.Begin_Step() -> B.Begin_Step() -> A.Step() -> B.Step()...

- Returns: N/A

```C#
public static void Beat() {}
```

</br>

#### Draw()

Draws contents on game window.

> The order of the event is as follows:
> Begin_Draw -> Draw -> End_Draw -> GUI_Draw
> 
> After the corresponding event for all Instances ends, the next event is executed.
> e.g. A.Begin_Draw() -> B.Begin_Draw() -> A.Draw() -> B.Draw()...

- Returns: N/A

```C#
public static void Draw() {}
```