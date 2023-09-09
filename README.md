# Swanston

![A sample rendering of the Swanston typeface in normal and bold weights, showing ASCII](/assets/swanston.png)

Swanston is a retro-inspired outline typeface designed to resemble bitmap fonts of times past while still being scalable to higher DPI monitors. Nearly all of the [WGL4](https://en.wikipedia.org/wiki/Windows_Glyph_List_4) set of glyphs is supported, including Latin, Greek, Cyrillic, and codepage 437 box-drawing and symbols. Both regular and bold weights are provided. Designed for use in terminals, all glyphs are 8x16, so Swanston can fit where raster fonts were formerly used.

### Usage

- Swanston is designed for and looks best at 16 pixel size or multiples thereof. On standard DPI Windows, this is 12pt. For other platforms, it is 16pt. Sizes smaller than 16 pixels will have compromised legibility, though some concessions are made for bitmap users. Larger non-multiple-of-16 sizes work fine, but might not be as clear.
- While Swanston resembles bitmap fonts, the font is intended to be seen anti-aliased. Bilevel rendering will look acceptable in the normal weight, but will not be easily distinguishable in the bold weight.
- The bold weight is intended to support terminals and IDEs that require that weight to exist. Its usage is discouraged, especially for white-on-black viewing environments. (I'm still trying to strike a good balance between legibility and distinguishability- there's not a lot of room to work with)

### Notes

Swanston is licenced under the SIL OFL, so freely use it for whatever you want.

Some font renderers might have trouble with Swanston. I'll try to fix things as they come up.

### Changes in v1.1
- Bold weight is now subtle, having been redrawn entirely.
	-	It looks better on white-on-black than black-on-white, so keep that in mind. It is more legible at smaller sizes but harder to distinguish between bold and normal.
- Combining mark stacking now works properly.
- Internally, references are now used more often.
- Bitmaps have been added for ppem sizes 8 to 15 in the regular weight.
	- Only ASCII and the box-drawing characters have bitmaps.
	- The bold weight does **not** have bitmaps added to it.
- TrueType Collection format added.
- Fonts hinted using ttfautohint, -a sss.