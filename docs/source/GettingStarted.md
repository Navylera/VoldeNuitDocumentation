# Getting Started

</br>

To Start Monogame project, see [this post](https://docs.monogame.net/articles/tutorials/building_2d_games/02_getting_started/index.html?tabs=windows).

### Install VoldeNuit by using NuGet

</br>

[Install VoldeNuit by using CLI](https://learn.microsoft.com/en-us/nuget/consume-packages/install-use-packages-nuget-cli);\
or if you are using VSCode, enter "> Nuget: Add NuGet Package" to Command Palette.

> VoldeNuit framework has dependencies on the [Magick.NET-Q8-AnyCPU](https://github.com/dlemstra/Magick.NET).\
 Follow the same steps for Magick.NET to resolve dependencies.

</br>

Next, add next code to projectname.csproj.

```C#
<ItemGroup>
...
<Reference Include="VoldeNuit"><HintPath>NightVision.dll</HintPath></Reference>
...
</ItemGroup>
```

</br></br>

### Initialize VoldeNuit

1. Open your Game class, and declare to use VoldeNuit.Framework.

```C#

using Microsoft.Xna.Framework;
using Microsoft.Xna.Framework.Graphics;
using Microsoft.Xna.Framework.Input;

using VoldeNuit.Framework;

namespace projectName;

```

1. Initialize VoldeNuit Invironments in Initialize() method.

```C#
protected override void Initialize() {

    // TODO: Add your initialization logic here

    Heart.InitResolution(1280, 800);

    Heart.InitMonoGameEnvironment("projectName", this, _graphics);

    Configuration.ANGLE_FORMAT = Configuration.AngleFormat.RADIAN;
    Configuration.COLOR_FORMAT = Configuration.ColorFormat.ARGB;

    Heart.InitEntryPoint(typeof(RoomTitle));

    base.Initialize();
}
```

1. Initialize SpriteBatch in LoadContent() method.

```C#
protected override void LoadContent() {

    _spriteBatch = new SpriteBatch(GraphicsDevice);

    Heart.InitSpriteBatch(_spriteBatch);

    // TODO: use this.Content to load your game content here
}
```

1. Add Heart.Beat() method in Update(GameTime gameTime) method.

```C#
protected override void Update(GameTime gameTime) {

    if (GamePad.GetState(PlayerIndex.One).Buttons.Back == ButtonState.Pressed || 
        Keyboard.GetState().IsKeyDown(Keys.Escape))
        Exit();

    // TODO: Add your update logic here

    Heart.Beat();

    base.Update(gameTime);
}
```

1. Add Heart.Draw() method in Draw(GameTime gameTime) method.

```C#
protected override void Draw(GameTime gameTime) {

    Heart.Draw();

    // TODO: Add your drawing code here

    base.Draw(gameTime);
}
```

1. Create new Room class.

```C#
using VoldeNuit.Framework.Display;

public class RoomTitle: Room {

    public RoomTitle() {

        Width  = 1280;
        Height = 800;

        RoomSpeed = 60;

        BackgroundColor = 0xffffff;
    }
}
```

1. Build and Run.

</br></br>

# After Initialization

You can find more informations and examples at VoldeNuit.Examples(WIP).