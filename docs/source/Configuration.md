# Configuration

namespace: [VoldeNuit.Framework](/Framework.md)

```C#
public static class Configuration
```

Configuration is static class that 
contains configuration about the overall game system.

### Static Properties

</br>

#### ANGLE_FORMAT
ANGLE_FORMAT contains that how to handle angle values. 

- RADIAN handles angle value from -float.Pi to float.Pi;
 calculated as 0 being right, float.Pi/2 being down, (-)float.Pi being left and -float.Pi/2 being down.
- DEGREE handles angle value from 0 to 360;
 calculated as 0 being right, 90 being down, 180 being left and 270 being up.
- LEGACY handles angle value from 0 to 360;
 calculated as 0 being right, 270 being down, 180 being left and 90 being up.

The default value is ColorFormat.RADIAN.

```C#
public static AngleFormat ANGLE_FORMAT { get; set; } = AngleFormat.RADIAN;

public enum AngleFormat {

    RADIAN,
    DEGREE,
    LEGACY
}
```

</br>

#### COLOR_FORMAT
COLOR_FORMAT contains that which order to interpret hexadecimal values to Color. 
The default value is ColorFormat.ARGB.

```C#
public static ColorFormat COLOR_FORMAT = ColorFormat.ARGB;

public enum ColorFormat {

    ARGB,
    BGRA,
    ABGR
}
```

</br>

#### ROUDNING

ROUDNING contains how to rounds number.
 The default value is [MidpointRounding.AwayFromZero](https://learn.microsoft.com/en-us/dotnet/api/system.midpointrounding?view=net-8.0).

```C#
public static MidpointRounding ROUNDING { get; set; } = MidpointRounding.AwayFromZero;
```

</br>

#### CONTENT_PATH_LINUX

Contains contents directory that used when running on Linux. Default value is "./Content/".

```C#
public static string CONTENT_PATH_LINUX { get; set; } = "./Content/";
```

</br>

#### CONTENT_PATH_WINDOWS

Contains contents directory that used when running on Windows. Default value is ".\\Content\\".

```C#
public static string CONTENT_PATH_WINDOWS { get; set; } = ".\\Content\\";
```

</br>

#### CONTENT_PATH_OTHERS

Contains contents directory that used when running on other os. Default value is "./Content/".

```C#
public static string CONTENT_PATH_OTHERS { get; set; } = "./Content/";
```