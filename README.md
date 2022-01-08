# Idobao ID67V2 keybaord

This board has thus far been released as 3 variants.

* [Idobao ID67V2](https://idobao.net/collections/65-layout/products/idobao-id67v2-65-hot-swappable-mechanical-keyboard-kit)
* [Idobao ID67 Crystal](https://idobao.net/collections/65-layout/products/idobao-id67-crystal-keyboard-kit-gasket-mount-version)
* [Idobao ID67 Bestype](https://idobao.net/collections/65-layout/products/idobao-id67-bestype-keyboard-kit-aluminum-with-brass-weight)

Code-wise it's the same as the Idobao ID *("V1")* ... but the RGB LED code is changed from the [RGB Lighting](https://docs.qmk.fm/#/feature_rgblight) to the [RGB Matrix](https://docs.qmk.fm/#/feature_rgb_matrix) library set.

* [QMK Keyboard](QMK/) files
* [VIA Keymap](VIA/) files

### QMK

This code contains the original QMK code for the [Idobao ID67](https://idobao.net/collections/65-layout/products/idobao-id67-65-hot-swappable-mechanical-keyboard-kit-1) ("V1"), but moved to a `v1` sub-folder.

The new RGB Matrix code resides in the `v2` sub-folder.

> I have made several attempts to pull this into QMK and have not had any luck.  Leaving this here for my personal usage.

### VIA

The ID67 keyboard is already in VIA - located at [`the-via/keyboards/src/other/id67/id67.json`](https://raw.githubusercontent.com/the-via/keyboards/0a7a2c0761aa8c6c128d160a541057a51c8d1fb3/src/other/id67/id67.json)

However, since the original code explicitly declares the `"lighting": "qmk_backlight_rgblight"` [property](https://caniusevia.com/docs/optional) it causes somewhat of an issue with VIA:

* When selecting "Lighting" on the left side bar the VIA app will display an empty window with no content.  This makes it impossible to use the app and one will need to close the app and relaunch it.

The VIA side-load JSON file in this project sets the `"lighting"` property to `"none"` as VIA does not support QMK Matrix library.

> As I have not been able to publish this QMK code I cannot submit it to VIA.  
Leaving this here for my personal usage.

* * *

Made with &#9829; by [Vino Rodrigues](https://github.com/vinorodrigues)
