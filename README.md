# NTX-Convertor
A program to convert the texture files (*.ntx) used specifically in Rovio's 3D Bounce series.
Currently a windows-only program.
Only supports conversion into **PNG** and back.

# Usage (v1.0)
The program is executed in this manner:
`PROGRAMNAME INPUT OPERATION OUTPUT`
where:
- **PROGRAMNAME** is the name of the actual executable - you may rename it to whatever you like.
- **INPUT** is the target file - whether an NTX or a PNG.
- **OPERATION** represents one of four possible operations:
  ```
  Code     Purpose
  p        Convert the input NTX file into a PNG.
  n        Convert the input PNG file into an RGB565 NTX file, without omitting the color 0x0000.
  N        Convert the input PNG file into an RGB565 NTX file, omitting the color 0x0000.
           This is used for transparency in textures. (Model textures only use RGB565 NTX files)
  i        Convert the input PNG file into an ARGB4444 NTX file.
           This is used for the UI. (GUI elements only use ARGB4444 NTX files)
  ```
- **OUTPUT** is the name of the output file --- extension included.

# Examples
```
ntxconvert worldmap_sheet_01.ntx p worldmap_sheet_01.png
ntxconvert "supercube texture.png" n supercube.ntx
```
