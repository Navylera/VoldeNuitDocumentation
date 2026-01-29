# Instance

namespace: [VoldeNuit.Framework.Instances](/Instances/Instances.md)

```C#
public abstract class Instance
```

Instance is abstract class that 
an object in a game must inherit, 
and includes various properties and methods for game.

>Note: In the following document, instances that inherited this class
 are referred to as "**Instance**", other instances
 are referred to as "**instance**".

>Note: For migration support from Gamemaker:Studio, 
Instance is automatically added to [instance_id](/Heart.md#instance-id) after created.\
For this feature, every Instance must inherit constructor of the parent Instance.

### Properties

</br>

#### id
id is read-only value that returns the reference of the Instance.

```C#
public Instance id { get => this; }
```

</br>

#### x
Contains x position of the Instance. The default value is 0.

```C#
public float x = 0f;
```

</br>

#### y
Contains y position of the Instance. The default value is 0.

```C#
public float y = 0f;
```

</br>

#### xprevious
Contains x value of the previous step.
 The x value just before the [Begin_Step](begin-step) executed is assign to xprevious.

```C#
public float xprevious;
```

</br>

#### yprevious
Contains y value of the previous step.
 The y value just before the [Begin_Step](begin-step) executed is assign to yprevious.

```C#
public float yprevious;
```

</br>

#### hspeed
Contains x-axis speed of the Instance. The default value is 0.\
 When hspeed is modified, the value of speed also changes.

```C#
public float hspeed = 0f;
```

</br>

#### vspeed
Contains y-axis speed of the Instance. The default value is 0.\
When vspeed is modified, the value of speed also changes.

```C#
public float vspeed = 0f;
```

</br>

#### speed
Contains speed of the Instance that movement in direction. The default value is 0.\
When speed is modified, the values of hspeed and vspeed also changes.\
If the value is negative, it moves in the opposite direction.

```C#
public float speed = 0f;
```

</br>

#### direction
Contains direction of the Instance that movement at speed. 
The default value is 0; The positive direction of the x-axis.
When direction is modified, the values of hspeed and vspeed also changes.

>Note: VoldeNuit provides three ways to express angles; radians, degrees, and legacy. The default is radians.\
>For more information, see [Configuration.ANGLE_FORMAT](/Configuration.md#angle-format).

```C#
public float direction = 0f;
```

</br>

#### friction
Contains friction of the Instance. The default value is 0.\
Before calculating the movement by the speed and the direction, 
the absolute value of the speed is subtracted by the friction.\
The minimum value of the absolute value of the speed subtracted by friction is 0.

```C#
public float friction = 0f;
```

</br>

#### solid
Contains whether the Instance is solid or not. The default value is false.\
If solid is true, it automatically calculates whether 
there is a collision when calculating the movement and stops 
when it collides with other solid Instances.

```C#
public bool solid = false;
```

</br>

#### collision
Contains whether the Instance calculates whether to collide or not. 
The default value is true; If Instance is solid, always returns true.\
If the collision is false, it is regarded as not having a collision box; 
is ignored in all collision decisions.

```C#
public bool collision = true;
```

</br>

#### depth

Contains the depth of the Instance. The default value is 0.\
Instance with large depth value is drawn on the window.
 If the depth values are the same, an early created Instance is drawn first.

```C#
public float depth = 0f;
```

</br>

#### sprite_index
Contains reference of the [Sprite](/Drawing/Sprite.md).
If sprite_index and [mask_index](mask-index) is null, it is regarded as not having a collision box; 
is ignored in all collision decisions.\
[draw_self()](draw-self) refers to this value.

>Note: When assign value to sprit_index,
 must assign instance reference returned by the [Instantiate(Type object_name)](instantiate-type-object-name) method.

```C#
public Sprite? sprite_index = null;
```

</br>

#### sprite_width
Contains width of the Instance's [Sprite](/Drawing/Sprite.md). 
If sprite_index is null, returns 0.

```C#
public readonly int sprite_width;
```

</br>

#### sprite_height
Contains height of the Instance's [Sprite](/Drawing/Sprite.md). 
If sprite_index is null, returns 0.

```C#
public readonly int sprite_height;
```
</br>

#### image_speed
Contains how image_index will increase with each step. The default value is 1.


```C#
public float image_speed = 1f;
```

</br>

#### image_index
Contains subimage index of Spritesheet. The default value is 0.\
It automatically increases by image_speed before [Begin_Step](begin-step).\
[draw_self()](draw-self) refers to this value.

```C#
public float image_index = 0f;
```

</br>

#### image_angle
Contains angle of the Instance's Sprite. The default value is 0; The positive direction of the x-axis.\
This value does not affect collision check.\
[draw_self()](draw-self) refers to this value.

>Note: VoldeNuit provides three ways to express angles; radians, degrees, and legacy. The default is radians.\
>For more information, see [Configuration.ANGLE_FORMAT](/Configuration.md#angle-format).

```C#
public float image_angle = 0f;
```

</br>

#### image_alpha
Contains alpha of Instance. The default value is 1. Value ranges from 0 to 1.\
[draw_self()](draw-self) refers to this value.

```C#
public float image_alpha = 1f;
```

</br>

#### image_number
image_alpha is read-only value that contains number of sub-images of Instance.

```C#
public int image_alpha;
```

</br>

#### image_xscale
Contains scale that direction of the x-axis. The default value is 1.\
If value is less than 0, image flips horizontally.\
This value does not affect collision check.\
[draw_self()](draw-self) refers to this value.

```C#
public float image_xscale = 1f;
```

</br>

#### image_yscale
Contains scale that direction of the y-axis. The default value is 1.\
If value is less than 0, image flips vertically.\
This value does not affect collision check.\
[draw_self()](draw-self) refers to this value.

```C#
public float image_yscale = 1f;
```

</br>

#### mask_index
Contains reference of Sprite that used for collision check. The default value is null.\
If mask_index is null, returns sprite_index.

```C#
public float mask_index = null;
```

</br></br>

### Methods

</br>

#### Create()
Runs when Instance is created.\
For more information, see [Heart.Beat()](/Heart.md#heart-beat).

```C#
public virtual void Create() {}
```

</br>

#### Begin_Step()
For more information, see [Heart.Beat()](/Heart.md#beat).

```C#
public virtual void Begin_Step() {}
```

</br>

#### End_Step()
For more information, see [Heart.Beat()](/Heart.md#beat).

```C#
public virtual void End_Step() {}
```

</br>

#### Begin_Draw()
For more information, see [Heart.Draw()](/Heart.md#draw).

```C#
public virtual void Begin_Draw() {}
```

</br>

#### Draw()
If Instance does not inherit this method, runs [draw_self()](draw-self) by default.\
For more information, see [Heart.Draw()](/Heart.md#draw).

```C#
public virtual void Draw() {}
```

</br>

#### End_Draw()
For more information, see [Heart.Draw()](/Heart.md#draw).

```C#
public virtual void End_Draw() {}
```

</br>

#### GUI_Draw()
In this method, position (0, 0) is always left-top of the game window and are unaffected by the scaling of any Viewport displayed on the screen.\
For more information, see [Heart.Draw()](/Heart.md#draw).

```C#
public virtual void GUI_Draw() {}
```

</br>

#### Destroy()
Runs when Instance is destroyed.\
For more information, see [Heart.Beat()](/Heart.md#beat).

```C#
public virtual void Destroy() {}
```

</br>

#### draw_self()
Draws an object with reference to the following properties.
- [sprite_index](sprite-index)
- [image_index](image-index)
- [x](x)
- [y](y)
- [image_xscale](image-xscale)
- [image_yscale](image-yscale)
- [image_angle](image-angle)
- [image_alpha](image-alpha)

```C#
public virtual void draw_self() {}
```

</br>

#### instance_place(float x, float y, Type object_name)
Returns reference of the Instance
 if it collides with the provided Type
 when it is moved to the provided positions.

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to move.|
|y|float|y position to move.|
|object_name|Type|Type of Instance to check collision.|

```C#
public Instance? instance_place(float x, float y, Type object_name) {}
```

</br>

#### instance_place(float x, float y, Instance id)
Returns reference of the Instance
 if it collides with the provided id
 when it is moved to the provided positions.

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to move.|
|y|float|y position to move.|
|id|Instance|Reference of Instance to check collision.|

```C#
public Instance? instance_place(float x, float y, Instance id) {}
```

</br>

#### instance_place_list(float x, float y, Type object_name)
Returns List of Instances same Type with provided Type that collided with the Instance
 when the Instance is moved to the provided positions.

- Returns: List\<Instance\> (List of collided Instance.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to move.|
|y|float|y position to move.|
|object_name|Type|Type of Instance to check collision.|

```C#
public List<Instance> instance_place_list(float x, float y, Type object_name) {}
```

</br>

#### activate()
Activate Instance. Deactivated Instances are excluded from all processes.

- Returns: N/A

```C#
public void activate() {}
```

</br>

#### deactivate()
Deactivate Instance. Deactivated Instances are excluded from all processes.

- Returns: N/A

```C#
public void deactivate() {}
```

</br></br>

### Static Methods

</br>

#### Instantiate(Type object_name)
Returns following type by converting it into reference of Instance.
- [Sprite](/Drawing/Sprite.md)
- [Font](/Drawing/Font.md)
- Instance
- [Sound](/Audio/Sound.md)

</br>

- Returns: dynamic? (Reference of instance converted from argument or null
 if passed argument is not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|object_name|Type|Type to convert to Instance.|

```C#
public static dynamic? Instantiate(Type object_name) {}
```

</br>

#### instance_create(float x, float y, Type object_name, float depth = 0f)
Returns reference of new Instance.

- Returns: Instance (reference of Instance created.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position of Instance.|
|y|float|y position of Instance.|
|object_name|Type|Type of Instance to create.|
|depth|float|depth of Instance. The default value is 0.|

```C#
public static Instance instance_create(float x, float y, Type object_name, float depth = 0f) {}
```

</br>

#### instance_exists(Type object_name)
Returns whether Instance of Type passed as argument exists in the game.

- Returns: bool (Whether Instance is exists.)

|Parameter|Type|Desc|
|---|---|---|
|object_name|Type|Type of Instance to check.|

```C#
public static bool instance_exists(Type object_name) {}
```

</br>

#### instance_exists(Instance id)
Returns whether Instance passed as argument exists in the game.

- Returns: bool (Whether Instance is exists.)

|Parameter|Type|Desc|
|---|---|---|
|id|Instance|reference of Instance to check.|

```C#
public static bool instance_exists(Instnace id) {}
```

</br>

#### instance_destroy(Type object_name, bool execute_event_flag = true)
Destroys all Instances that is same or inherited from Type passed as argument.

- Returns: bool (Whether Instances are exists and are destroyed.)

|Parameter|Type|Desc|
|---|---|---|
|object_name|Type|Type of Instance to destroy.|
|execute_event_flag|bool|Whether execute [Destroy()](destroy) method. The default value is true.|

```C#
public static bool instance_destroy(Type object_name, bool execute_event_flag = true) {}
```

</br>

#### instance_destroy(Instance id, bool execute_event_flag = true)
Destroys Instance that passed as argument.

- Returns: bool (Whether Instances are exists and are destroyed.)

|Parameter|Type|Desc|
|---|---|---|
|id|Instance|Reference of Instance to destroy.|
|execute_event_flag|bool|Whether execute [Destroy()](destroy) method. The default value is true.|

```C#
public static bool instance_destroy(Instance id, bool execute_event_flag = true) {}
```

</br>

#### instance_position(float x, float y, Type object_name)
Returns reference of the Instance
 if the Instance exists on provided positions.

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to check collision.|
|y|float|y position to check collision.|
|object_name|Type|Type of Instance to check collision.|

```C#
public static Instance? instance_position(float x, float y, Type object_name) {}
```

</br>

#### instance_position(float x, float y, Instance id)
Returns reference of the Instance
 if the Instance exists on provided positions.

- Returns: Instance? (Reference of collided Instance, null if no collided Instance exists or not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to check collision.|
|y|float|y position to check collision.|
|id|Instance|Reference of Instance to check collision.|

```C#
public static Instance? instance_position(float x, float y, Instance id) {}
```

</br>

#### instance_position_list(float x, float y, Type object_name)
Returns List of Instances same with Type passed as argument that on the position.

- Returns: List\<Instance\> (List of collided Instances.)

|Parameter|Type|Desc|
|---|---|---|
|x|float|x position to check collision.|
|y|float|y position to check collision.|
|object_name|Type|Type of Instance to check collision.|

```C#
public static List<Instance> instance_position(float x, float y, Type object_name) {}
```

</br>

#### instance_find(Type object_name, int index = 0)
Returns reference of Instance that same with Type passed as argument.

- Returns: Instance? (Reference of Instance that same with Type passed as argument or null
 if passed argument is not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|object_name|Type|Type of Instance to find.|
|index|int|Index of the Instance to find. The default value is 0.|

```C#
public static Instance? instance_find?(Type object_name, int index = 0) {}
```

</br>

#### instance_find(Instance id)
Returns reference of Instance that same with Type passed as argument.

- Returns: Instance? (Reference of Instance that same with passed as argument or null
 if passed argument is not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|id|Type|Reference of Instance to find.|

```C#
public static Instance? instance_find?(Instance id) {}
```

</br>

#### instance_find_list(Type object_name)
Returns List of Instances same with Type passed as argument.

- Returns: Instance? (Reference of Instance that same with Type passed as argument or null
 if passed argument is not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|object_name|Type|Type of Instance to find.|
|index|int|Index of the Instance to find. The default value is 0.|

```C#
public static List<Instance> instance_find?(Type object_name, int index = 0) {}
```

</br></br>

### Properties Alias

</br>

#### ID
Alias of [id](id).
```C#
public Instance ID;
```

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

#### XPrevious
Alias of [xprevious](xprevious).
```C#
public float XPrevious;
```

</br>

#### YPrevious
Alias of [yprevious](yprevious).
```C#
public float YPrevious;
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

</br>

#### Speed
Alias of [speed](speed).

```C#
public float Speed;
```

</br>

#### Direction
Alias of [direction](direction).

```C#
public float Direction;
```

</br>

#### Friction
Alias of [friction](friction).

```C#
public float Friction;
```

</br>

#### isSolid
Alias of [solid](solid).

```C#
public bool isSolid;
```

</br>

#### isCollidable
Alias of [collision](collision).

```C#
public bool isCollidable;
```

</br>

#### Depth
Alias of [depth](depth).

```C#
public float Depth;
```

</br>

#### SpriteIndex
Alias of [sprite_index](sprite-index).

```C#
public Sprite? SpriteIndex;
```

</br>

#### ImageSpeed
Alias of [image_speed](image-speed).


```C#
public float ImageSpeed;
```

</br>

#### ImageIndex
Alias of [image_index](image-index).

```C#
public float ImageIndex.
```

</br>

#### ImageAngle
Alias of [image_angle](image-angle).

```C#
public float ImageAngle;
```

</br>

#### ImageAlpha
Alias of [image_alpha](image-alpha).

```C#
public float ImageAlpha;
```

</br>

#### ImageNumber
Alias of [image_number](image-number).

```C#
public int ImageNumber;
```

</br>

#### ImageXScale
Alias of [image_xscale](image-xscale).

```C#
public float ImageXScale;
```

</br>

#### ImageYScale
Alias of [image_yscale](image-yscale).

```C#
public float ImageYScale;
```

</br>

#### Mask
Alias of [mask_index](mask-index).

```C#
public float Mask;
```

</br></br>

### Methods Alias

</br>

#### DrawSelf()
Alias of [draw_self()](draw-self).

- Returns: N/A

```C#
public virtual void DrawSelf() {}
```

</br>

#### GetInstanceMeetsWithAt(float X, float Y, Type objectName)
Alias of [instance_place(float x, float y, Type object_name)](instance-place-float-x-float-y-type-object-name).

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to move.|
|Y|float|y position to move.|
|objectName|Type|Type of Instance to check collision.|
```C#
public Instance? GetInstanceMeetsWithAt(float X, float Y, Type objectName) {}
```

</br>

#### GetInstanceMeetsWithAt(float X, float Y, Instance ID)
Alias of [instance_place(float x, float y, Instance ID)](instance-place-float-x-float-y-instance-id).

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to move.|
|Y|float|y position to move.|
|ID|Instance|Reference of Instance to check collision.|
```C#
public Instance? GetInstanceMeetsWithAt(float X, float Y, Instance ID) {}
```

</br>

#### GetListMeetsWithAt(float X, float Y, Type objectName)
Alias of [instance_place_list(float x, float y, Type object_name)](instance-place-list-float-x-float-y-type-object-name).

- Returns: List\<Instance\> (List of collided Instance.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to move.|
|Y|float|y position to move.|
|objectName|Type|Type of Instance to check collision.|
```C#
public List<Instance> GetListMeetsWithAt(float X, float Y, Type objectName) {}
```

</br>

#### Activate()
Alias of [activate()](activate).

- Returns: N/A

```C#
public void Activate() {}
```

</br>

#### Deactivate()
Alias of [deactivate()](deactivate).

- Returns: N/A

```C#
public void Deactivate() {}
```

</br></br>

### Static Methods Alias

</br>

#### CreateInstance(float X, float Y, Type objectName, float depth = 0f)
Alias of [instance_create(float x, float y, Type object_name, float depth = 0f)](instance-create-float-x-float-y-type-object-name-int-depth-0f).

- Returns: Instance (reference of Instance created.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position of Instance.|
|Y|float|y position of Instance.|
|objectName|Type|Type of Instance to create.|
|depth|float|depth of Instance. The default value is 0.|

```C#
public static Instance CreateInstance(float X, float Y, Type objectName, float depth = 0f) {}
```

</br>

#### IsInstanceExists(Type objectName)
Alias of [instance_exists(Type object_name)](instance-exists-type-object-name).

- Returns: bool (Whether Instance is exists.)

|Parameter|Type|Desc|
|---|---|---|
|objectName|Type|Type of Instance to check.|

```C#
public static bool IsInstanceExists(Type objectName) {}
```

</br>

#### IsInstanceExists(Instance ID)
Alias of [instance_exists(Instance id)](instance-exists-instance-id).

- Returns: bool (Whether Instance is exists.)

|Parameter|Type|Desc|
|---|---|---|
|ID|Instance|reference of Instance to check.|

```C#
public static bool IsInstanceExists(Instance ID) {}
```

</br>

#### Destroy(Type objectName, bool eventFlag = true)
Alias of [instance_destroy(Type object_name, bool execute_event_flag = true)](instance-destroy-type-object-name-bool-execute-event-flag-true).

- Returns: bool (Whether Instances are exists and are destroyed.)

|Parameter|Type|Desc|
|---|---|---|
|objectName|Type|Type of Instance to destroy.|
|eventFlag|bool|Whether execute [Destroy()](destroy) method. The default value is true.|

```C#
public static bool Destroy(Type objectName, bool eventFlag = true) {}
```

</br>

#### Destroy(Instance ID, bool eventFlag = true)
Alias of [instance_destroy(Instance id, bool execute_event_flag = true)](instance-destroy-instance-id-bool-execute-event-flag-true).

- Returns: bool (Whether Instances are exists and are destroyed.)

|Parameter|Type|Desc|
|---|---|---|
|ID|Instance|Reference of Instance to destroy.|
|eventFlag|bool|Whether execute [Destroy()](destroy) method. The default value is true.|

```C#
public static bool Destroy(Instance ID, bool eventFlag = true) {}
```

</br>

#### GetInstanceOnPosition(float X, float Y, Type objectName)
Alias of [instance_position(float x, float y, Type object_name)](instance-position-float-x-float-y-type-object-name).

- Returns: Instance? (Reference of first collided Instance, null if no collided Instance exists or not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to check collision.|
|X|float|y position to check collision.|
|objectName|Type|Type of Instance to check collision.|

```C#
public static Instance? GetInstanceOnPosition(float X, float Y, Type objectName) {}
```

</br>

#### instance_position(float x, float y, Instance id)
Alias of [instance_position(float x, float y, Instance id)](instance-position-float-x-float-y-instance-id).

- Returns: Instance? (Reference of collided Instance, null if no collided Instance exists or not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to check collision.|
|Y|float|y position to check collision.|
|ID|Instance|Reference of Instance to check collision.|

```C#
public static Instance? GetInstanceOnPosition(float X, float Y, Instance ID) {}
```

</br>

#### GetListOnPosition(float X, float Y, Type objectName)
Alias of [instance_position_list(float x, float y, Type object_name)](instance-position-list-float-x-float-y-type-object-name).

- Returns: List\<Instance\> (List of collided Instances.)

|Parameter|Type|Desc|
|---|---|---|
|X|float|x position to check collision.|
|Y|float|y position to check collision.|
|objectName|Type|Type of Instance to check collision.|

```C#
public static List<Instance> GetListOnPosition(float X, float Y, Type objectName) {}
```

</br>

#### FindInstance(Type objectName, int index = 0)
Alias of [instance_find(Type object_name, int index = 0)](instance-find-type-object-name-int-index-0).

- Returns: Instance? (Reference of Instance that same with Type passed as argument or null
 if passed argument is not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|objectName|Type|Type of Instance to find.|
|index|int|Index of the Instance to find. The default value is 0.|

```C#
public static Instance? FindInstance(Type objectName, int index = 0) {}
```

</br>

#### FindInstance(Type ID)
Alias of [instance_find(Instance id)](instance-find-instance-id).

- Returns: Instance? (Reference of Instance that same with passed as argument or null
 if passed argument is not valid Instance.)

|Parameter|Type|Desc|
|---|---|---|
|ID|Type|Reference of Instance to find.|

```C#
public static Instance? FindInstance(Type ID) {}
```

</br>

#### GetListInstance(Type objectName)
Alias of [instance_find_list(Type object_name)](instance-find-list-type-object-name).

- Returns: Instance? (Reference of Instance that same with Type passed as argument or null
 if passed argument is not valid Type.)

|Parameter|Type|Desc|
|---|---|---|
|objectName|Type|Type of Instance to find.|
|index|int|Index of the Instance to find. The default value is 0.|

```C#
public static List<Instance> GetListInstance(Type objectName) {}
```
