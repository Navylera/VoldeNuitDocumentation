# Listener

namespace: [VoldeNuit.Framework.Audio](/Audio/Audio.md)

```C#
public class Listener
```

Contains about 3D audio.
 In 3D audio, Listener has the direction and positions of the instance
 to which the sound is heard.

>Note: By default, there is one Listener automatically created; Index is 0.

### Properties

</br>

#### x
Contains x position of the Listener. The default value is 0.
```C#
public float x = 0f;
```

</br>

#### y
Contains y position of the Listener. The default value is 0.
```C#
public float y = 0f;
```

</br>

#### hspeed
Contains x-axis speed of the Instance. The default value is 0.\
When you assign a value to hspeed, the value of speed also change.

>Note: This value is used for the 3D sound calculation; Listener does not actually move.

```C#
public float hspeed = 0f;
```

</br>

#### vspeed
Contains y-axis speed of the Instance. The default value is 0.\
When you assign a value to vspeed, the value of speed also change.

>Note: This value is used for the 3D sound calculation; Listener does not actually move.

```C#
public float vspeed = 0f;
```

</br>

#### speed
Contains speed of the Instance that movement in direction. The default value is 0.\
When you assign a value to speed, the values of hspeed and vspeed also change.\
If the value is negative, it is assumed that moving in the opposite direction.

>Note: This value is used for the 3D sound calculation; Listener does not actually move.

```C#
public float speed = 0f;
```

</br>

#### direction
Contains direction of the Listener that movement at speed. 
The default value is 0; The positive direction of the x-axis.
When you assign a value to direction, the values of hspeed and vspeed also change.
>Note: VoldeNuit provides three ways to express angles; radians, degrees, and legacy. The default is radians.\
>For more information, see [Configuration.ANGLE_FORMAT](/Configuration.md#color-format).

>Note: This value is used for the 3D sound calculation; Listener does not actually move.

```C#
public float direction = 0f;
```

</br>

#### pan_amount
Contains the coefficient of panning. The default value is 0.15. Value ranges from 0 to 1.

```C#
public float pan_amount = .15f;
```

</br>

#### lookat
Contains vector that indicating where the listener is facing. It is automatically normalized when the value is assigned.

```C#
public Vector2 lookat;
```

</br>

#### lookat_x
Contains x value of lookat.

```C#
public Vector2 lookat_x;
```

</br>

#### lookat_y
Contains y value of lookat.

```C#
public Vector2 lookat_y;
```

</br></br>

### Methods

</br>

#### sync_to(Instancd id)
Synchronizes following properties of the Emitter and Instance.

- x
- y
- speed
- direction

</br>

- Returns: N/A

```C#
public void sync_to(Instance id) {}
```

</br></br>

### Static Methods

</br>

#### audio_listener_position(float x, float y)
Sets position of the default Listener.

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to set.|
|y|float|y position to set.|

- Returns: N/A

```C#
public static void audio_listener_position(float x, float y) {}
```

</br>

#### audio_listener_set_position(Listener listener, float x, float y)
Sets position of the Listener.

|Parameter|Type|Desc|
|---|---|---|
|listener|Listener|Reference of the Listener.|
|x|float|x position to set.|
|y|float|y position to set.|

- Returns: N/A

```C#
public static void audio_listener_position(Listener listener, float x, float y) {}
```

</br>

#### audio_listener_velocity(float vx, float vy)
Sets speed of the default Listener.

|Parameter|Type|Desc|
|---|---|---|
|vx|float|hspeed to set.|
|vy|float|vspeed to set.|

- Returns: N/A

```C#
public static void audio_listener_velocity(float vx, float vy) {}
```

</br>

#### audio_listener_set_velocity(Listener listener, float vx, float vy)
Sets speed of the Listener.

|Parameter|Type|Desc|
|---|---|---|
|listener|Listener|Reference of the Listener.|
|vx|float|hspeed to set.|
|vy|float|vspeed to set.|

- Returns: N/A

```C#
public static void audio_listener_velocity(Listener listener, float vx, float vy) {}
```

</br>

#### audio_listener_orientation(float lookat_x, float lookat_y)
Sets orientation of the default Listener.

|Parameter|Type|Desc|
|---|---|---|
|lookat_x|float|x position to set.|
|lookat_y|float|y position to set.|

- Returns: N/A

```C#
public static void audio_listener_orientation(float lookat_x, float lookat_y) {}
```

</br>

#### audio_listener_set_orientation(Listener listener, float lookat_x, float lookat_y)
Sets orientation of the Listener.

|Parameter|Type|Desc|
|---|---|---|
|listener|Listener|Reference of the Listener.|
|lookat_x|float|x position to set.|
|lookat_y|float|y position to set.|

- Returns: N/A

```C#
public static void audio_listener_orientation(Listener listener, float lookat_x, float lookat_y) {}
```

</br></br>

### Properties Alias

</br>

#### X
Alias of [x](x).

```C#
public float X;
```

</br>

#### Y
Alias of [y](y).

```C#
public float Y;
```

</br>

#### HSpeed
Alias of [hspeed](hspeed).

```C#
public float HSpeed;
```

</br>

#### VSpeed
Alias of [vspeed](vspeed).

```C#
public float VSpeed;
```

</br></br>

#### Speed
Alias of [speed](speed).

```C#
public float speed;
```

</br>

#### Direction
Alias of [direction](direction).

```C#
public float direction;
```

</br>

#### PanAmount
Alias of [pan_amount](pan-amount).

```C#
public float PanAmount;
```

#### LookAt
Alias of [lookat](lookat).

```C#
public float LookAt;
```

</br></br>

### Methods Alias

</br>

#### SyncTo(Instancd ID)
Alias of [sync_to(Instance id)](sync-to-instance-id).

- Returns: N/A

```C#
public void SyncTo(Instance ID) {}
```