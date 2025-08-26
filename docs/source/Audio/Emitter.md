# Emitter

namespace: [VoldeNuit.Framework.Audio](/Audio/Audio.md)

```C#
public class Emitter
```

Contains about 3D audio.
 In 3D audio, Emitter has the positions at audio is played and the gain-model.

### Properties

</br>

#### x
Contains x position of the Emitter. The default value is 0.

```C#
public float x = 0f;
```

</br>

#### y
Contains y position of the Emitter. The default value is 0.

```C#
public float y = 0f;
```

</br>

#### hspeed
Contains x-axis speed of the Emitter. The default value is 0.\
When you assign a value to hspeed, the value of speed also change.

>Note: This value is used for the 3D sound calculation; Emitter does not actually move.

```C#
public float hspeed = 0f;
```

</br>

#### vspeed
Contains y-axis speed of the Emitter. The default value is 0.\
When you assign a value to vspeed, the value of speed also change.

>Note: This value is used for the 3D sound calculation; Emitter does not actually move.

```C#
public float vspeed = 0f;
```

</br>

#### speed
Contains speed of the Emitter that movement in direction. The default value is 0.\
When you assign a value to speed, the values of hspeed and vspeed also change.\
If the value is negative, it is assumed that moving in the opposite direction.

>Note: This value is used for the 3D sound calculation; Emitter does not actually move.

```C#
public float speed = 0f;
```

</br>

#### direction
Contains direction of the Emitter that movement at speed. 
The default value is 0; The positive direction of the x-axis.
When you assign a value to direction, the values of hspeed and vspeed also change.
>Note: VoldeNuit provides three ways to express angles; radians, degrees, and legacy. The default is radians.\
>For more information, see [Configuration.ANGLE_FORMAT](/Configuration.md#color-format).

>Note: This value is used for the 3D sound calculation; Emitter does not actually move.

```C#
public float direction = 0f;
```

</br>

#### speed_sound
Contains speed of the sound. The default value is 0.\
The sign of the value is ignored. If the value is zero, the Doppler effect is ignored.

>Note: This value is only used for the 3D sound calculation.

```C#
public float speed_sound = 0f;
```

</br>

#### falloff
Contains the gain-model in sound over distance.
>Note: For information of falloff-model, see <https://manual.gamemaker.io/lts/en/GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_falloff_set_model.htm>.

```C#
public Falloff falloff = Falloff.NONE;

public enum Falloff {

    NONE,
    LINEAR_DISTANCE,
    LINEAR_DISTANCE_CLAMPED,
    INVERSE_DISTANCE,
    INVERSE_DISTANCE_CLAMPED,
    INVERSE_DISTANCE_SCALED,
    EXPONENT_DISTANCE,
    EXPONENT_DISTANCE_CLAMPED,
    EXPONENT_DISTANCE_SCALED,
}
```

</br>

#### falloff_reference
Contains distance value; 
 maximum volume is the value at that distance.
```C#
public float falloff_reference;
```

</br>

#### falloff_max
Contains maximum distance at which sound is transmitted.
```C#
public float falloff_max;
```

</br>

#### falloff_factor
Contains value that affect the increase or decrease of the sound. 
The default value is 1.
```C#
public float falloff_factor = 1f;
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

#### SoundSpeed
Alias of [speed_sound](speed-sound).

```C#
public float SoundSpeed;
```

</br>

#### FallOff
Alias of [falloff](falloff).

```C#
public Falloff FallOff;
```

</br>

#### FallOffReference
Alias of [falloff_reference](falloff-reference).

```C#
public float FallOffReference;
```

</br>

#### FallOffMax
Alias of [falloff_max](falloff-max).
```C#
public float FallOffMax;
```

</br>

#### FallOffFactor
Alias of [falloff_factor](falloff-factor).
```C#
public float FallOffFactor;
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

