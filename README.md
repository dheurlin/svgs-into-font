# svgs-into-font

A FontForge script which inserts a list of SVGs as glyphs into the private area
(E000-F8FF) of an existing font. I use it to generate fonts for my status bar so
I get my custom icons as well as all the normal letters without having to rely
on fallback fonts.

## Requirements

This is a FontForge script, so you need to have FontForge installed.

## Usage

```
./insert.pe [input-font] glyph1 glyph2 ...
```

When given `filename.ext` as input, will output the patched font as
`filename-patched.ext`.

If you have a bunch of SVGs in a directory and want to insert them all into the
font, you can run:

```
ls -d [full-path-to-svg-dir] | xargs ./insert.pe
```
