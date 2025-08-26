# Path

namespace: [VoldeNuit.Framework.MotionPlanning](/MotionPlanning/MotionPlanning.md)

```C#
public struct Path
```

Path class that containing path data as [Vector2](https://docs.monogame.net/api/Microsoft.Xna.Framework.Vector2.html) list.

### Properties

#### Count
Count is read-only value that contains length of the path.

```C#
public int Count { get; }
```

</br></br>

### Methods

</br>

#### Path()
Constructor. Creates new Path and returns it.

- Returns: Path

```C#
public Path() {}
```

</br>

#### this[int i]
Gets or Add value of the cell at index that passed as argument.

- Returns: dynamic (get => Vector2; set => N/A.)

|Parameter|Type|Desc|
|---|---|---|
|i|int|Index of the data.|

```C#
public Vector2 this[int i] { get; set; }
```

</br>

#### Add(Vector2 v)
Adds Vector2 data passed as argument at end of the path.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|Vector2|v|Vector2 data to add.|

```C#
public void Add(Vector2 v) {}
```

</br>

```C#
public void Clear() {}
```

</br></br>

### Static Methods

</br>

#### path_add()
Constructor. Creates new Path and returns it.

- Returns: Path

```C#
public static Path path_add() {}
```

</br>

#### public static bool mp_grid_path(Grid grid, Path path, int xstart, int ystart, int xdest, int ydest, bool diagonal) {}

Attemps to create path from start to destination and assigns it to path that passed as argument. 
If destination is not reachable, returns false.

- Returns: bool (Whether destination is reachable or not.)

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|
|path|Path|Reference of the path to get path data.|
|xstart|int|x position to start.|
|ystart|int|y position to start.|
|xdest|int|x position to end.|
|ydest|int|y position to end.|
|diagonal|bool|Whether allow to move diagonal or not.|

```C#
public static bool mp_grid_path(Grid grid, Path path, int xstart, int ystart, int xdest, int ydest, bool diagonal) {}
```