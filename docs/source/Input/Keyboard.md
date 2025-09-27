# Keyboard

namespace: [VoldeNuit.Framework.Input](/Input/Input.md)

```C#
public static class Keyboard
```

Contains methods for keyboard input.

### Static Properties

</br>

#### Keyboard Constants

Constants to check state of the keyboard.

|Constant|In MonoGame.Input.Keys(or byte)|
|---|---|
|vk_nokey|None|
|vk_anykey|255|
|AnyKey|255|
|vk_left|Left|
|vk_right|Right|
|vk_up|Up|
|vk_down|Down|
|vk_enter|Enter|
|vk_escape|Escape|
|vk_space|Space|
|vk_shift|159|
|Shift|159|
|vk_control|158|
|Control|158|
|vk_alt|157|
|Alt|157|
|vk_backspace|Back|
|vk_tab|Tab|
|vk_home|Home|
|vk_end|End|
|vk_delete|Delete|
|vk_insert|Insert|
|vk_pageup|PageUp|
|vk_pagedown|PageDown|
|vk_pause|Pause|
|vk_printscreen|PrintScreen|
|vk_f1|F1|
|vk_f2|F2|
|vk_f3|F3|
|vk_f4|F4|
|vk_f5|F5|
|vk_f6|F6|
|vk_f7|F7|
|vk_f8|F8|
|vk_f9|F9|
|vk_f10|F10|
|vk_f11|F11|
|vk_f12|F12|
|vk_numpad0|NumPad0|
|vk_numpad1|NumPad1|
|vk_numpad2|NumPad2|
|vk_numpad3|NumPad3|
|vk_numpad4|NumPad4|
|vk_numpad5|NumPad5|
|vk_numpad6|NumPad6|
|vk_numpad7|NumPad7|
|vk_numpad8|NumPad8|
|vk_numpad9|NumPad9|
|vk_multiply|Multiply|
|vk_divide|Divide|
|vk_add|Add|
|vk_subtract|Subtract|
|vk_decimal|Keys.Decimal|
|vk_lshift|LeftShift|
|vk_lcontrol|LeftControl|
|vk_lalt|LeftAlt|
|vk_rshift|RightShift|
|vk_rcontrol|RightControl|
|vk_ralt|RightAlt|

</br>

#### vk_lastkey
Contains last key value pressed.

```C#
public static byte vk_lastkey { get; set; } = vk_nokey;
```

</br></br>

### Static Methods

</br>

#### ord(char c)
Returns argument that converted to a byte value for checking keyboard state.

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|c|char|A character to check input.|

```C#
public static byte ord(char c) {}
```

</br>

#### keyboard_check(byte key)
Returns whether the key is pressed or not.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check input.|

```C#
public static bool keyboard_check(byte input) {}
```

</br>

#### keyboard_check_pressed(byte key)
Returns true when the key is pressed and was not pressed in the previous Step.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check pressed.|

```C#
public static bool keyboard_check_pressed(byte input) {}
```

</br>

#### keyboard_check_released(byte key)
Returns true when the key is released and was pressed in the previous Step.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check released.|

```C#
public static bool keyboard_check_released(byte key) {}
```

</br>

#### keyboard_key_press(byte key)
Changes key state that passed as arugument to pressed.

>Note: The state changed by this method remains for current frame only, and the state returned by [Keyboard.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Keyboard.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to change state.|

```C#
public static void keyboard_key_press(byte key) {}
```

</br>

#### keyboard_key_release(byte key)
Changes key state that passed as arugument to released.

>Note: The state changed by this method remains for current frame only, and the state returned by [Keyboard.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Keyboard.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to change state.|

```C#
public static void keyboard_key_release(byte key) {}
```

</br>

#### keyboard_clear(byte key)
Clears current keyboard state.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to clear.|

```C#
public static void keyboard_clear(byte input) {}
```

</br>

#### io_clear()
Clears current input state.

> Obsolete: This method will be removed in the next major update. Please use the [UniversalInput.io_clear()](/Input/UniversalInput.md#io-clear) instead."

- Returns: N/A

```C#
public static void io_clear() {}
```

</br></br>

### Static Properties Alias

</br>

#### LastKey
Alias of [vk_lastkey](vk-lastkey).

```C#
public static byte LastKey;
```

</br></br>

### Static Methods Alias

</br>

#### CharToByte(char c)
Alias of [ord(char c)](ord-char-c).

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|c|char|A character to check input.|

```C#
public static byte CharToByte(char c) {}
```

</br>

#### HasKeyInput(byte key)
Alias of [keyboard_check(byte input)](keyboard-check-byte-input).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check input.|

```C#
public static bool HasKeyInput(byte key) {}
```

</br>

#### HasKeyPressed(byte input)
Alias of [keyboard_check_pressed(byte key)](keyboard-check-pressed-byte-key).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check pressed.|

```C#
public static bool HasKeyPressed(byte input) {}
```

</br>

#### HasKeyReleased(byte key)
Alias of [keyboard_check_released(byte key)](keyboard-check-released-byte-key).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to check released.|

```C#
public static bool HasKeyReleased(byte key) {}
```

</br>

#### PressKey(byte key)
Alias of [keyboard_key_press(byte key)](keyboard-key-press-byte-key).

>Note: The state changed by this method remains for current frame only, and the state returned by [Keyboard.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Keyboard.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to change state.|

```C#
public static void PressKey(byte key) {}
```

</br>

#### ReleaseKey(byte key)
Alias of [keyboard_key_release(byte key)](keyboard-key-release-byte-key).

>Note: The state changed by this method remains for current frame only, and the state returned by [Keyboard.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Keyboard.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to change state.|

```C#
public static void ReleaseKey(byte key) {}
```

</br>

#### ClearKey(byte input)
Alias of [keyboard_clear(byte key)](keyboard-clear-byte-key).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|key|byte|byte data to clear.|

```C#
public static void ClearKey(byte input) {}
```

</br>

#### ClearIO()

> Obsolete: This method will be removed in the next major update. Please use the [UniversalInput.ClearIO()](/Input/UniversalInput.md#cleario) instead."

Alias of [io_clear()](io-clear).

- Returns: N/A

```C#
public static void ClearIO() {}
```