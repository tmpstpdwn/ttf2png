# TTF to PNG Converter

This script converts a single glyph from a TrueType font to a PNG image using ImageMagick. It allows you to specify the font, glyph, color, and output file path.

## Why ??

I made this small script to help me in displaying nerd font glyphs in [dunst](https://github.com/dunst-project/dunst) as dunst only has support for png's for notifcation icons.

## Dependancies

- ImageMagick: Ensure that the magick command is available on your system. You can install ImageMagick using package managers like apt, yum, or brew.

## Installation

move/copy `src/ttf2png` to a directory under `$PATH` varible for global access. 

## Usage

``` bash
ttf2png.sh -f FONT -g GLYPH -c COLOR -p OUTPUT
```
- -f FONT: Name of the TTF font (without extension).
- -g GLYPH: Glyph to convert.
- -c COLOR: Color of the glyph (hex code, optional). If not provided, the default color is used.
- -p OUTPUT: Output file path for the PNG image.

Example:

``` bash
ttf2png -f "MononokiNerdFont-Bold" -g "󰦗" -p "/tmp/downloadicon"
```

## Color Source

- If color provided explicitly then that color will be used for png foreground.  
- If not, The script attempts to source colors from [`shwal`](https://github.com/tmpstpdwn/Shwal) or [`pywal`](https://github.com/dylanaraps/pywal) if they are installed.
- If neither of the above works then the default foreground color is set to #FFFFFF.

## License

This project is licensed under the GPL3 License - see the [LICENSE](LICENSE) file for details.
