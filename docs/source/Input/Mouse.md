# Mouse

namespace: [VoldeNuit.Framework.Input](/Input/Input.md)

```C#
public static class Mouse
```

Contains methods for mouse input.

### Static Properties

</br>

#### Mouse Constants

Constants to check state of the mouse.

|Constant|int value|
|---|---|
|mb_left|0|
|mb_middle|1|
|mb_right|2|
|mb_none|3|
|mb_any|4|

</br>

#### mouse_x
Contains x position of the mouse.

>Note: This property ignores state of camera.

```C#
public static int mouse_x { get; set; }
```

</br>

#### mouse_y
Contains y position of the mouse.

>Note: This property ignores state of camera.

```C#
public static int mouse_y { get; set; }
```

</br>

#### mouse_lastbutton
Contains last button value pressed.

```C#
public static byte mouse_lastbutton { get; set; } = mb_none;
```

</br></br>

### Static Methods

</br>

#### mouse_x_on(Camera camera)
Returns x position of the mouse that relative to camera that passed as argument.

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|camera|Camera|camera to check position.|

```C#
public static int mouse_x_on(Camera camera) {}
```
</br>

#### mouse_y_on(Camera camera)
Returns y position of the mouse that relative to camera that passed as argument.

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|camera|Camera|camera to check position.|

```C#
public static int mouse_y_on(Camera camera) {}
```

</br>

#### mouse_check_button(int mb)
Returns whether the button is pressed or not.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mb|int|int data to check input.|

```C#
public static bool mouse_check_button(int mb) {}
```

</br>

#### mouse_check_button_pressed(int mb)
Returns true when the button is pressed and was not pressed in the previous Step.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mb|int|int data to check input.|

```C#
public static bool mouse_check_button_pressed(int mb) {}
```

</br>

#### mouse_check_button_released(int mb)
Returns true when the button is released and was pressed in the previous Step.

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mb|int|int data to check input.|

```C#
public static bool mouse_check_button_released(int mb) {}
```

</br>

#### mouse_button_press(int mb)
Changes button state that passed as arugument to pressed.

>Note: The state changed by this method remains for current frame only, and the state returned by [Mouse.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Mouse.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|mb|int|int data to change state.|

```C#
public static void mouse_button_press(int mb) {}
```

</br>

#### mouse_button_release(int mb)
Changes button state that passed as arugument to released.

>Note: The state changed by this method remains for current frame only, and the state returned by [Mouse.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Mouse.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|mb|int|int data to change state.|

```C#
public static void mouse_button_release(int mb) {}
```

</br>

#### mouse_wheel_up()
Returns whether mouse wheel is scrolled up.

- Returns: bool (whether mouse wheel is scrolled up.)

```C#
public static void mouse_wheel_up() {}
```

</br>

#### mouse_wheel_down()
Returns whether mouse wheel is scrolled down.

- Returns: bool (whether mouse wheel is scrolled down.)

```C#
public static void mouse_wheel_down() {}
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

### Static Properties Alias

</br>

#### Mouse Constants Alias

Alias of [Mouse Constatns](mouse-constants).

|Constant|int value|
|---|---|
|Left|0|
|Middle|1|
|Right|2|
|None|3|
|Any|4|

</br>

#### X
Alias of [mouse_x](mouse-x).

>Note: This property ignores state of camera.

```C#
public static int X { get; set; }
```

</br>

#### Y
Alias of [mouse_y](mouse_y).

>Note: This property ignores state of camera.

```C#
public static int Y { get; set; }
```

</br>

#### LastButton
Alias of [mouse_lastbutton](mouse-lastbutton).

```C#
public static byte mouse_lastbutton { get; set; };
```

</br></br>

### Static Methods Alias

</br>

#### XOnCamera(Camera camera)
Alias of [mouse_x_on(Camera camera)](mouse-x-on-camera-camera).

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|camera|Camera|camera to check position.|

```C#
public static int XOnCamera(Camera camera) {}
```

</br>

#### YOnCamera(Camera camera)
Alias of [mouse_y_on(Camera camera)](mouse-y-on-camera-camera).

- Returns: byte

|Parameter|Type|Desc|
|---|---|---|
|camera|Camera|camera to check position.|

```C#
public static int YOnCamera(Camera camera) {}
```

</br>

#### HasButtonInput(int mouseButton)
Alias of [mouse_check_button(int mb)](mouse-check-button-int-mb).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mouseButton|int|int data to check input.|

```C#
public static bool HasButtonInput(int mouseButton) {}
```

</br>

#### HasButtonPressed(int mouseButton)
Alias of [mouse_check_button_pressed(int mb)](mouse-check-button-pressed-int-mb).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mouseButton|int|int data to check input.|

```C#
public static bool HasButtonPressed(int mouseButton) {}
```

</br>

#### HasButtonReleased(int mouseButton)
Alias of [mouse_check_button_released(int mouseButton)](mouse-check-button-released-int-mb).

- Returns: bool

|Parameter|Type|Desc|
|---|---|---|
|mouseButton|int|int data to check input.|

```C#
public static bool HasButtonReleased(int mouseButton) {}
```

</br>

#### PressButton(int mouseButton)
Alias of [mouse_button_press(int mb)](mouse-button-press-int-mb).

>Note: The state changed by this method remains for current frame only, and the state returned by [Mouse.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Mouse.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|mouseButton|int|int data to change state.|

```C#
public static void PressButton(int mb) {}
```

</br>

#### ReleaseButton(int mouseButton)
Alias of [mouse_button_release(int mb)](mouse-button-release-int-mb).

>Note: The state changed by this method remains for current frame only, and the state returned by [Mouse.GetState()](https://docs.monogame.net/api/Microsoft.Xna.Framework.Input.Mouse.html) is not change.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|mouseButton|int|int data to change state.|

```C#
public static void ReleaseButton(int mb) {}
```

</br>

#### HasWheelUp()
Alias of [mouse_wheel_up()](mouse-wheel-up).

- Returns: bool (whether mouse wheel is scrolled up.)

```C#
public static void mouse_wheel_up() {}
```

</br>

#### HasWheelDown()
Alias of [mouse_wheel_down()](mouse-wheel-down).

- Returns: bool (whether mouse wheel is scrolled down.)

```C#
public static void HasWheelDown() {}
```
</br></br>