# lovefuser

This simple shell script automates creating "fused" application executables
for games created against the [LÖVE 2D][love] engine. It's primarily
intended for generating macOS application bundles, but soon it can also be
used to create standalone executables for Windows, too.

Note that, as of this writing, you need to run this script _on a Mac_ in
order to generate macOS app bundles, because this script uses the
Darwin-only commands plutil(1) and sips(1). But, I do plan on making a more
portable version. This will eventually allow LÖVE users to generate Mac
*and* Windows executables from any environment that can run Bourne shell
scripts, such as Linux.


## Usage

`lovefuser` requires the user to provide the path to a "pristine" (i.e.,
unmodified) version of the LOVE application, and some details required to
make the new game distinct from it.

In general, it follows the [pattern established in LOVE's wiki.][lovewiki]

```
lovefuser: usage: lovefuser [options ...] game.love
  --help                show this message
  --love PATH           location of pristine love.app
  --identifer STRING    desired CFBundleIdentifier (reverse domain name)
  --name STRING         desired CFBundleName
```


## License

This script is released under a 2-clause BSD-style license. Read the
script's header for details.


[love]: love2d.org
[lovewiki]: https://love2d.org/wiki/Game_Distribution
