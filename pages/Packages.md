Packages are a mostly unused feature in Principia, outside of the built-in puzzle package.

Packages are, as can probably be figured out, a series of levels packaged together. They can be selectable from a level selector, with a specific amount of levels being unlocked at a particular time (see the puzzle package). Alternatively the first level can act as an in-game level selector, using the [[Pkg Warp]] and [[Pkg Status]] objects to manage level completion and warping (akin to a SM64-like level selector world).

Initially during Principia's development it was intended for players to create their own packages and upload them to the community site using the game's Package Manager dialog ^(PC only)^. However this was seemingly scrapped around the game's release and users' package listings were quietly commented out from the community site.

## Creating packages
The package format has been documented ([Kaitai](https://github.com/principia-game/kaitai/blob/master/kaitai/ppkg.ksy)) and there exists a tool called [package-creator](https://github.com/principia-game/package-creator) which can generate a .ppkg file from a JSON file with data for the package.

With the release of the Principia source code, a previously inaccessible Package Manager dialog now exists if you build the PC version in Debug mode. It can create and manage packages, but has some bugs as it assumedly was written for a much older version of Principia.

## Distributing packages
principia-web has preliminary support for packages ([see package list](/listpackages)) but does not currently support uploading packages or display the packages publicly. Right now there only exists some testing packages made by ROllerozxa but if you would like to work with packages and upload one, please contact him and it can be solved.

## Technical package info
Packages consist of one .ppkg file which contain package metadata and a list of level IDs. The game will pick levels from the current level namespace, so if a package is launched from the built-in `pkg/main/` namespace it will look for levels in `lvl/main/`, and vice versa. When launching a package from a community site, it will download all package levels in bulk from a special endpoint that should not check for a level's locked status.

In the built-in package level selector, the level previews are pre-rendered and loaded from a 256x256 uncompressed greyscale bitmap inside of the level file. It is generated on each save from the current camera position when saving. This can theoretically be edited to adjust or improve the level previews, although there does not exist a tool right now to do so automatically.
