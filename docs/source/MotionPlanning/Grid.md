# Grid

namespace: [VoldeNuit.Framework.MotionPlanning](/MotionPlanning/MotionPlanning.md)

```C#
public class Grid
```

Grid class for containing map data.

### Properties

</br>

#### Grid Constants

Constants for cell data.

|Constant|int value|
|---|---|
|SOLID|-1|
|UNDEFINED|-2|

</br>

#### x
Contains x position of the grid.

```C#
public int x;
```

</br>

#### y
Contains y position of the grid.

```C#
public int y;
```

</br>

#### cellwidth
Contains width of cell of the grid.

```C#
public int cellwidth;
```

</br>

#### cellheight
Contains height of cell of the grid.

```C#
public int cellheight;
```

</br></br>

### Methods

</br>

#### Grid(int x, int y, int hcells, int vcells, int cellwidth, int cellheight)
Constructor. Creates new Grid with properties and returns it.

- Returns: Grid

|Parameter|Type|Desc|
|---|---|---|
|x|int|x position of grid.|
|y|int|y position of grid.|
|hcells|int|Number of horizontal cells.|
|vcells|int|Number of vertical cells.|
|cellwidth|int|Width of cell.|
|cellheight|int|Height of cell.|

```C#
public Grid(int x, int y, int hcells, int vcells, int cellwidth, int cellheight) {}
```

</br>

#### this[int h, int v]
Gets or Sets value of the cell on position that passed as argument.

- Returns: dynamic (get => int; set => N/A.)

|Parameter|Type|Desc|
|---|---|---|
|h|int|Horizontal position of cell.|
|v|int|Vertical position of cell.|

```C#
public int this[int h, int v] { get; set; }
```

</br>

#### InitRegion(int x, int y, int width, int height)
Sets value of the cells as [SOLID](grid-constants) within region on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|x|int|x position of the region.|
|y|int|y position of the region.|
|width|int|Width of the region.|
|height|int|Height of the region.|

```C#
public void InitRegion(int x, int y, int width, int height) {}
```

</br>

#### InitRegion(Rectangle region)
Sets value of the cells as [SOLID](grid-constants) within region on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|region|Rectangle|Data of the region.|

```C#
public void InitRegion(Rectangle region) {}
```

</br>

#### public void InitInstance(Instance instance, bool precision)
Sets value of the cells as [SOLID](grid-constants) within [Instance](/Instances/Instance.md) on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|instance|Instance|Reference of the Instance.|
|precision|bool|Whether check collision based on pixel data of the Instance's Sprite or not.|

```C#
public void InitInstance(Instance instance, bool precision) {}
```

</br>

#### Clear()
Sets value of all cells as [UNDEFINED](grid-constants).

- Returns: N/A


```C#
public void Clear() {}
```

</br>

#### Destroy()
Destroys the grid.

- Returns: N/A


```C#
public void Destroy() {}
```

</br></br>

### Static Methods

</br>

#### mp_grid_create(int x, int y, int hcells, int vcells, int cellwidth, int cellheight)
Constructor. Creates new Grid with properties and returns it.

- Returns: Grid

|Parameter|Type|Desc|
|---|---|---|
|x|int|x position of grid.|
|y|int|y position of grid.|
|hcells|int|Number of horizontal cells.|
|vcells|int|Number of vertical cells.|
|cellwidth|int|Width of cell.|
|cellheight|int|Height of cell.|

```C#
public static Grid mp_grid_create(int x, int y, int hcells, int vcells, int cellwidth, int cellheight) {}
```

</br>

#### mp_grid_add_cell(Grid grid, int h, int v)
Sets value of the cell on position that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|
|h|int|Horizontal position of cell.|
|v|int|Vertical position of cell.|

```C#
public static void mp_grid_add_cell(Grid grid, int h, int v) {}
```

</br>

#### mp_grid_add_rectangle(Grid grid, int x, int y, int width, int height)
Sets value of the cells as [SOLID](grid-constants) within region on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|
|x|int|x position of the region.|
|y|int|y position of the region.|
|width|int|Width of the region.|
|height|int|Height of the region.|

```C#
public static void mp_grid_add_rectangle(Grid grid, int x, int y, int width, int height) {}
```

</br>

#### mp_grid_add_region(Grid grid, Rectangle region)
Sets value of the cells as [SOLID](grid-constants) within region on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|
|region|Rectangle|Data of the region.|

```C#
public static void mp_grid_add_region(Grid grid, Rectangle region) {}
```

</br>

#### public void mp_grid_add_instances(Grid grid, Instance instance, bool precision)
Sets value of the cells as [SOLID](grid-constants) within [Instance](/Instances/Instance.md) on room that passed as argument.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|
|instance|Instance|Reference of the Instance.|
|precision|bool|Whether check collision based on pixel data of the Instance's Sprite or not.|

```C#
public static void mp_grid_add_instances(Grid grid, Instance instance, bool precision) {}
```

</br>

#### mp_grid_clear_all(Grid grid)
Sets value of all cells as [UNDEFINED](grid-constants).

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|


```C#
public static void mp_grid_clear_all(Grid grid) {}
```

</br>

#### mp_grid_destroy(Grid grid)
Destroys the grid.

- Returns: N/A

|Parameter|Type|Desc|
|---|---|---|
|grid|Grid|Reference of the grid.|

```C#
public void mp_grid_destroy(Grid grid) {}
```

</br></br>

### Properties Alias

</br>

#### X
Alias of [x](x).

```C#
public int X;
```

</br>

#### Y
Alias of [y](y).

```C#
public int Y;
```

</br>

#### HCells
Alias of [hcells](hcells).

```C#
public int HCells;
```

</br>

#### VCells
Alias of [vcells](vcells).

```C#
public int VCells;
```

</br>

#### CellWidth
Alias of [cellwidth](cellwidth).

```C#
public int CellWidth;
```

</br>

#### CellHeight
Alias of [cellheight](cellheight).

```C#
public int CellHeight;
```