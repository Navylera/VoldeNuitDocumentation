# SoundInstance

namespace: [VoldeNuit.Framework.Audio](/Audio/Audio.md)

```C#
public class SoundInstance
```

Contains about values that playing sound.

>Note: When SoundInstance stops, it is automatically disposed.

### Properties

</br>

#### Emitter
Contains reference of [Emitter](./Emitter.md).

```C#
public Emitter? emitter;
```

</br>

#### listener
Contains reference of [Listener](./Listener.md).

```C#
public Listener? listener;
```

</br>

#### gain
Contains gain of SoundInstance. The default value is 1. the value ranges from -10 to 10.

```C#
public float gain = 1f;
```

</br>

#### pitch
Contains pitch of SoundInstance. The default value is 0. the value ranges from -10 to 10.

```C#
public float gain = 0f;
```

</br>

#### pan
Contains pan of SoundInstance. The default value is 0 (center). the value ranges from -1 (left) to 1 (right).

```C#
public float gain = 0f;
```

</br>

#### loop
Contains whether repeat SoundInstance. The default value is false.

```C#
public bool loop = false;
```

</br></br>

### Properties Alias

</br>

#### Emitter
Alias of [emitter](emitter).

```C#
public Emitter? Emitter;
```

</br>

#### Listener
Alias of [listener](listener).

```C#
public Listener? Listener;
```

</br>

#### Gain
Alias of [gain](gain).

```C#
public float Gain;
```

</br>

#### Pitch
Alias of [pitch](pitch).

```C#
public float Pitch;
```

</br>

#### Pan
Alias of [Pan](pan).

```C#
public float Pan;
```

</br>

#### Loop
Alias of [loop](loop).

```C#
public bool Loop;
```
