# WASTE NO SPACE

Waste No Space is a theme for Godot projects, originally by [Flatus at Itch.io](https://flatus.itch.io/waste-no-space-gui). I've upgraded it to work with Godot 4.2 since they don't seem to be developing it anymore and made some minor adjustments I felt made things look cleaner. Also includes an Aseprite file for the GUI's spritesheet.

![](sample.gif)

## Installation

Clone or [download](https://github.com/iamswampthing/waste-no-space/archive/refs/heads/master.zip) the repository and copy `addons/` into the root of your project folder.

### Configuration

#### Applying the theme

* **If you would like to apply the theme to your entire project**, you can do so by navigating to `Project > Project Settings... > General (Make sure "Advanced Settings" is checked) > GUI > Theme > Custom` and use the file dialog to select `waste_no_space.tres`.

* **If you would like to apply this theme to specific controls**, do so from `Inspector > Control > Theme > Theme` and either drag `waste_no_space.tres` into the dropdown or select it using the `Load` option.

#### Configuring texture filtering

If the UI elements look blurry, you have two options: either disable texture filtering for the entire project, or for the parent `CanvasItem` of your GUI.

* **To disable texture filtering for the entire project**, go to `Project > Project Settings... > General > Rendering > Textures > Default Texture Filter` and select "Nearest".

* **To disable texture filtering for specific controls** navigate to the highest-level node in your GUI's tree that has the `CanvasItem` class and in the inspector navigate to `CanvasItem > Texture > Filter` where you should select "Nearest".

#### Scaling the UI

By default, the ui elements are pretty small. This isn't an issue if you're working on a [pixel art game with a low viewport size](https://docs.godotengine.org/en/stable/tutorials/rendering/multiple_resolutions.html#desktop-game) but for most other use cases it's a problem. There are two methods for scaling it up:

* **Per-control**: Select the parent control of your UI elements, and then in the inspector navigate to `Control > Layout > Transform > Scale` and increase as needed.

* **For the entire game**: Navigate to `Project > Project Settings... > Display > Window > Scale` and increase as needed.

I typically use a scale of 2-3 for a 1920x1080 viewport size. If you're unsure of which method to use, you should read [Multiple Resolutions](https://docs.godotengine.org/en/stable/tutorials/rendering/multiple_resolutions.html) in the Godot docs.

## License

This project is released under its original terms. For more details, see [LICENSE.markdown](LICENSE.markdown). The included font is licensed separately from the rest of the project. If you choose to use it, you should make sure to comply with [the terms of its license](fonts/LICENSE.markdown).
