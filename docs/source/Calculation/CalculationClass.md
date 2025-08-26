# Calculation

namespace: [VoldeNuit.Framework.Calculation](/Calculation/Calculation.md)

```C#
public static class Calculation
```

### Static Methods

</br>

#### point_direction(float x1, float y1, float x2, float y2)
Returns angle between two points.

>Note: VoldeNuit provides three ways to express angles; radians, degrees, and legacy. The default is radians.\
>For more information, see [Configuration.ANGLE_FORMAT](/Configuration.md#angle-format).

- Returns: float (angle from (x1, y1) to (x2, y2).)

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of start point.|
|y1|float|y position of start point.|
|x2|float|x position of end point.|
|y2|float|y position of end point.|

```C#
public static float point_direction(float x1, float y1, float x2, float y2) {}
```

</br>

#### point_distance(float x1, float y1, float x2, float y2)
Returns distance between two points.

- Returns: float (distance.)

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of first point.|
|y1|float|y position of first point.|
|x2|float|x position of second point.|
|y2|float|y position of second point.|

```C#
public static float point_distance(float x1, float y1, float x2, float y2) {}
```

</br>

#### radian_to_legacy(float radian)
Converts radian to [Legacy type](/Configuration.md#angle-format) and returns it.

- Returns: float (Legacy type angle.)

|Parameter|Type|Desc|
|---|---|---|
|radian|float|radian to convert.|

```C#
public static float radian_to_legacy(float radian) {}
```

</br>

#### legacy_to_radian(float degree)
Converts [Legacy type](/Configuration.md#angle-format) to radian returns it.

- Returns: float (radian.)

|Parameter|Type|Desc|
|---|---|---|
|degree|float|legacy type degree to convert.|

```C#
public static float legacy_to_radian(float degree) {}
```

</br></br>

### Static Methods Alias

</br>

#### GetDirection(float x1, float y1, float x2, float y2)
Alias of [point_direction(float x1, float y1, float x2, float y2)](point-direction-float-x1-float-y1-float-x2-float-y2).

- Returns: float (angle from (x1, y1) to (x2, y2).)

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of start point.|
|y1|float|y position of start point.|
|x2|float|x position of end point.|
|y2|float|y position of end point.|

```C#
public static float GetDirection(float x1, float y1, float x2, float y2) {}
```

</br>

#### GetDistance(float x1, float y1, float x2, float y2)
Alias of [point_distance(float x1, float y1, float x2, float y2)](point-distance-float-x1-float-y1-float-x2-float-y2).

- Returns: float (distance.)

|Parameter|Type|Desc|
|---|---|---|
|x1|float|x position of first point.|
|y1|float|y position of first point.|
|x2|float|x position of second point.|
|y2|float|y position of second point.|

```C#
public static float GetDistance(float x1, float y1, float x2, float y2) {}
```

</br>

#### RadiansToLegacyDegrees(float radian)
Alias of [radian_to_legacy(float radian)](radian-to-legacy-float-radian).

- Returns: float (Legacy type angle.)

|Parameter|Type|Desc|
|---|---|---|
|radian|float|radian to convert.|

```C#
public static float RadiansToLegacyDegrees(float radian) {}
```

</br>

#### LegacyDegreesToRadians(float degree)
Alias of [legacy_to_radian(float degree)](legacy-to-radian-float-degree).

- Returns: float (radian.)

|Parameter|Type|Desc|
|---|---|---|
|degree|float|legacy type degree to convert.|

```C#
public static float LegacyDegreesToRadians(float degree) {}
```
