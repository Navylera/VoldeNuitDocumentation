# Sound

namespace: [VoldeNuit.Framework.Audio](/Audio/Audio.md)

```C#
public class Sound
```

Contains sound for [SoundInstance](./SoundInstance.md).

>Note: Sound class is created when that Sound is referenced for the first time,
 and audio file is loaded at the same time.
 If no value is assigned to [sound_path](sound-path), tracks file with the same name as the class name.\
supported filename extensions are [.xnb](https://docs.monogame.net/articles/getting_to_know/whatis/content_pipeline/) and .wav.\
The default path is "[Configuration.CONTENT_PATH_LINUX](/Configuration.md#content-path-linux)+Sound" on Linux,
 "[Configuration.CONTENT_PATH_WINDOWS](/Configuration.md#content-path-windows)+Sound" on Windows,
 "[Configuration.CONTENT_PATH_UNIVERSAL](/Configuration.md#content-path-universal)+Sound" on the others. 

### Properties

</br>

#### sound_path
Contains path of sound file. The default value is null. It can be only assigned once.
 If no value is assigned, tracks files with the same name as the class name.

```C#
public string? sound_path { get; init; } = null;
```

#### volume
Contains volume of original audio. The default value is 1.\
Any change in this value affects all [SoundInstance](./SoundInstance.md)s that reference it.
 As a result, volume of SoundInstance is 'Sound.volume*[SoundInstance.gain](/SoundInstance.md#gain);'.

```C#
public float volume = 1f;
```

</br></br>

### Static Methods

</br>

#### audio_play_sound(Sound sound, bool loop = false)
Plays Sound passed as argument.

- Returns: Reference of [SoundInstance](./SoundInstance.md).

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to play.|
|loop|bool|Whether Sound is loop or not. The default value is false.|

```C#
public static SoundInstance audio_play_sound(Sound sound, bool loop = false) {}
```

</br>

#### audio_play_sound_ext(Sound sound, Emitter emitter, Listener listener, bool loop = false)
Plays Sound that passed as argument by applying 3d sound.

- Returns: Reference of [SoundInstance](./SoundInstance.md).

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to play.|
|emitter|Emitter|Reference of Emitter.|
|listener|Listener|Reference of Listener.|
|loop|bool|Whether Sound is loop or not. The default value is false.|

```C#
public static SoundInstance audio_play_sound_ext(Sound sound, Emitter emitter, Listener listener, bool loop = false) {}
```

</br>

#### audio_pause_sound(Sound sound)
Pauses all [SoundInstance](./SoundInstance.md) that match passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to pause.|

```C#
public static void audio_pause_sound(Sound sound) {}
```

</br>

#### audio_pause_sound(SoundInstance soundinstance)
Pauses [SoundInstance](./SoundInstance.md) passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundinstance|SoundInstance|Reference of SoundInstance to pause.|

```C#
public static void audio_pause_sound(SoundInstance soundinstance) {}
```

</br>

#### audio_pause_all()
Pauses all [SoundInstance](./SoundInstance.md).

- Returns: N/A

```C#
public static void audio_pause_all() {}
```

</br>

#### audio_resume_sound(Sound sound)
Resumes all [SoundInstance](./SoundInstance.md) that match passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to resume.|

```C#
public static void audio_resume_sound(Sound sound) {}
```

</br>

#### audio_resume_sound(SoundInstance soundinstance)
Resumes [SoundInstance](./SoundInstance.md) passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundinstance|SoundInstance|Reference of SoundInstance to resume.|

```C#
public static void audio_resume_sound(SoundInstance soundinstance) {}
```

</br>

#### audio_resume_all()
Resumes all [SoundInstance](./SoundInstance.md).

- Returns: N/A

```C#
public static void audio_resume_all() {}
```

</br>

#### audio_stop_sound(Sound sound)
Stops all [SoundInstance](./SoundInstance.md) that match passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to stop.|

```C#
public static void audio_stop_sound(Sound sound) {}
```

</br>

#### audio_stop_sound(SoundInstance soundinstance)
Stops [SoundInstance](./SoundInstance.md) passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundinstance|SoundInstance|Reference of SoundInstance to stop.|

```C#
public static void audio_stop_sound(SoundInstance soundinstance) {}
```

</br>

#### audio_stop_all()
Stops all [SoundInstance](./SoundInstance.md).

- Returns: N/A

```C#
public static void audio_stop_all() {}
```

</br>

#### audio_is_playing(Sound sound)
Returns whether Sound passed as argument is playing.

- Returns: bool (Whether Sound is playing.)

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to check.|

```C#
public static bool audio_is_playing(Sound sound) {}
```

</br>

#### audio_is_playing(SoundInstance soundinstance)
Returns whether SoundInstance passed as argument is playing.

- Returns: bool (Whether SoundInstance is playing.)

|Parameter|Type|Desc|
|---|---|---|
|soundinstance|SoundInstance|Reference of SoundInstance to check.|

```C#
public static bool audio_is_playing(SoundInstance soundinstance) {}
```

</br>

#### audio_is_paused(Sound sound)
Returns whether Sound passed as argument is paused.

- Returns: bool (Whether Sound is paused.)

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to check.|

```C#
public static bool audio_is_paused(Sound sound) {}
```

</br>

#### audio_is_paused(SoundInstance soundinstance)
Returns whether SoundInstance passed as argument is paused.

- Returns: bool (Whether SoundInstance is paused.)

|Parameter|Type|Desc|
|---|---|---|
|soundinstance|SoundInstance|Reference of SoundInstance to check.|

```C#
public static bool audio_is_paused(SoundInstance soundinstance) {}
```

</br></br>

### Properties Alias

</br>

#### Volume
Alias of [volume](volume).

```C#
public float Volume;
```

</br>

#### SoundPath
Alias of [sound_path](sound-path).

```C#
public string? SoundPath;
```

</br></br>

### Static Methods Alias

</br>

#### SoundPlay(Sound sound, bool loop = false)
Alias of [audio_play_sound(Sound sound, bool loop = false)](audio-play-sound-sound-sound-bool-loop-false).

- Returns: Reference of [SoundInstance](./SoundInstance.md).

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to play.|
|loop|bool|Whether Sound is loop or not. The default value is false.|

```C#
public static SoundInstance SoundPlay(Sound sound, bool loop = false) {}
```

</br>

#### SoundInstance SoundPlay(Sound sound, Emitter emitter, Listener listener, bool loop = false)
Alias of [audio_play_sound_ext(Sound sound, Emitter emitter, Listener listener, bool loop = false)](audio-play-sound-ext-sound-sound-emitter-emitter-listener-listener-bool-loop-false).

- Returns: Reference of [SoundInstance](./SoundInstance.md).

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to play.|
|emitter|Emitter|Reference of Emitter.|
|listener|Listener|Reference of Listener.|
|loop|bool|Whether Sound is loop or not. The default value is false.|

```C#
public static SoundInstance SoundPlay(Sound sound, Emitter emitter, Listener listener, bool loop = false) {}
```

</br>

#### SoundPause()
Alias of [audio_pause_all()](audio-pause-all).

- Returns: N/A

```C#
public static void SoundPause() {}
```

</br>

#### SoundPause(Sound sound)
Alias of [audio_pause_sound(Sound sound)](audio-pause-sound-sound-sound).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to pause.|

```C#
public static void SoundPause(Sound sound) {}
```

</br>

#### SoundPause(SoundInstance soundInstance)
Alias of [audio_pause_sound(SoundInstance soundinstance)](audio-pause-sound-soundinstance-soundinstance).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundInstance|SoundInstance|Reference of SoundInstance to pause.|

```C#
public static void SoundPause(SoundInstance soundInstance) {}
```

</br>

#### SoundResume()
Alias of [audio_resume_all()](audio-resume-all).

- Returns: N/A

```C#
public static void SoundResume() {}
```

</br>

#### SoundResume(Sound sound)
Alias of [audio_resume_sound(Sound sound)](audio-resume-sound-sound-sound).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to resume.|

```C#
public static void SoundResume(Sound sound) {}
```

</br>

#### SoundResume(SoundInstance soundInstance)
Alias of [audio_resume_sound(SoundInstance soundinstance)](audio-resume-sound-soundinstance-soundinstance).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundInstance|SoundInstance|Reference of SoundInstance to resume.|

```C#
public static void SoundResume(SoundInstance soundInstance) {}
```

</br>

#### SoundStop()
Alias of [audio_stop_all()](audio-stop-all).

- Returns: N/A

```C#
public static void SoundStop() {}
```

</br>

#### SoundStop(Sound sound)
Alias of [audio_stop_sound(Sound sound)](audio-stop-sound-sound-sound).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to stop.|

```C#
public static void SoundStop(Sound sound) {}
```

</br>

#### SoundStop(SoundInstance soundInstance)
Alias of [audio_stop_sound(SoundInstance soundinstance)](audio-stop-sound-soundinstance-soundinstance).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|soundInstance|SoundInstance|Reference of SoundInstance to stop.|

```C#
public static void SoundStop(SoundInstance soundInstance) {}
```

</br>

#### IsSoundPlaying(Sound sound)
Alias of [audio_is_playing(Sound sound)](audio-is-playing-sound-sound).

- Returns: bool (Whether Sound is playing.)

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to check.|

```C#
public static bool IsSoundPlaying(Sound sound) {}
```

</br>

#### IsSoundPlaying(SoundInstance soundInstance)
Alias of [audio_is_playing(Sound sound)](audio-is-playing-soundinstance-soundinstance).

- Returns: bool (Whether SoundInstance is playing.)

|Parameter|Type|Desc|
|---|---|---|
|soundInstance|SoundInstance|Reference of SoundInstance to check.|

```C#
public static bool IsSoundPlaying(SoundInstance soundInstance) {}
```

</br>

#### IsSoundPaused(Sound sound)
Alias of [audio_is_paused(Sound sound)](audio-is-paused-sound-sound).

- Returns: bool (Whether Sound is paused.)

|Parameter|Type|Desc|
|---|---|---|
|sound|Sound|Reference of Sound to check.|

```C#
public static bool IsSoundPaused(Sound sound) {}
```

</br>

#### IsSoundPaused(SoundInstance soundInstance)
Alias of [audio_is_paused(SoundInstance soundinstance)](audio-is-paused-soundinstance-soundinstance).

- Returns: bool (Whether SoundInstance is paused.)

|Parameter|Type|Desc|
|---|---|---|
|soundInstance|SoundInstance|Reference of SoundInstance to check.|

```C#
public static bool IsSoundPaused(SoundInstance soundInstance) {}
```
