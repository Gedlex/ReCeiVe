# ReCeiVe

The LuaLaTex class ReCeiVe provides a wide variety of possible cv structures and allows the user to change many details easily. The class is written in such a manner that it should not be necessary to alternate it in any way in order to get the desired cv layout.

Credits also go to Claud D. Park aka posquit0 and Jan Vorisek on whose CV templates the ReCeiVe classe is based on.

## Document Class

Initialise the document class ReCeiVe.
```
\documentclass[<Sidebar Position>]{ReCeiVe}
```
 * `Sidebar Position` - Position of of the sidebar (optional) (`leftPos`, `rightPos`)

## Margins

If one wants to use a paper size other than Letter or different paper margins than the predefined ones, one must use the following command.
```
\geometry[<Sidebar Width>]{<Standard Commands of the Geometry Package>}
```
* `Sidebar Width` - Width of the sidebar (optional). Predefined value: 6 cm

## Colors
Change the color of text objects and highlighted objects using HTML
```
\definecolor{<Color Object>}{HTML}{414141}
```
Or using predefined colors
```
\colorlet{<Color Object>}{<Color>}
```
* `Color` - Predefined colors (`darkgray`, `gray`, `lightgray`, `lightblue`, `orange`, `red`, `concrete`)

| Color Object | Header | Footer | Entry | Honor | Sidebar | Letter |
| :----------: | :----: | :----: | :---: | :---: | :-----: | :----: |
| `tex` | *positions, socials* | - | *location, item* | *location* | *text* | *section, text* |
| `darktext` | *word, quote* | - | *title* | *position* | *skills, language* | *title, name* |
| `graytext` | - | - | *position, date* | *title, date* | - | *recipient, date, enclosure* |
| `lighttext` | - | *left, center, right* | - | - | - | - |
| `highlight` | *name, socials* | - | - | - | *photo, titles* | - |

## Picture
To load a picture use the following command
```
\photo[<Shape>,<Frame>,<Fill>,<Position>]{<Size>,<Image Path>}
```
* `Shape` - Shape of the image (`circle`, `rectangle`)
* `Frame` -  Define whether the image is framed or not (`edge`, `noedge`)
* `Fill` -  Higlighte the image background with the `highlight`color (`fill`, `nofill`) (only works with png's or pdf's)
* `Position` - Position of the image (`left`, `right`, `sidebar`) (left and right only works with centred header)
* `Size` - Size of the image e.g. 2.5 cm
* `Image Path` Path where the image is stored e.g. pics/pp2.pdf

## Background
Set a background that is loaded on every page
```
\background[<Opacity>]{<Background Image Path>}
```
* `Opacity` Opacity of the background e.g. 0.15
* `Background Image Path` Path to the background image e.g. pics/background5.pdf

## Header
