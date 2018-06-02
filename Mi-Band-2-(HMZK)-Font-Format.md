The Mi Band 2 uses a special Font format, which is documented below:

## Overview

The HMZK Format has three sections:

 * Header
 * Character section, an array of the characters available in the font in order
 * Bitmap section, a list of 16x16 bitmaps in the same order as the Character Section


## Header

The file starts with a 16 byte header:
`484d 5a4b 01ff ffff ffff ffff ffff 7438`

The first two bytes (`484d 5a4b`) are the "magic number" and spell out "HMZK" in ascii (possible means HuaMi ZiKu, HuaMi character library)

The next five bytes (`01ff ffff ffff ffff ffff`) are of an unknown purpose, likely just padding.

The last two bytes are a 16bit little-endian integer describing the offset of the bitmap section from the character section in bytes (to find the absolute location of the bitmap section, add 16 to this number). This value can also be interpreted as length of the character section in bytes.

### Character Section

This Section contains an array of 16bit (widechar) values:

`2000 2100 2200 2300 2400 2500 2600 2700`

Each of these elements is a little endian utf-16 like encoded character (note: UTF-16 specifies prefix bytes e.g. `0xFF 0xFE`. These are omitted here)

### Bitmap Section

`0000 0000 1000 1000 1000 1000 1000 1000`
`1000 1000 1000 1000 0000 0000 1000 1000`

Each Bitmap consists of 16 16bit big endian (!!!) values. Each 16bit value represents one row of the bitmap. The above thus expands to:

```
................
................
...#............
...#............
...#............
...#............
...#............
...#............
...#............
...#............
...#............
...#............
................
................
...#............
...#............
```