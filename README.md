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
Change the color of text objects and highlighted objects as the font.
```
\colorlet{<Color Object>}{<Color>}
```
* `Color` - Predefined colors (`darkgray`, `gray`, `lightgray`, `lightblue`, `orange`, `red`, `concrete`)

| Color Object | Header | Footer | Entry | Honor | Sidebar | Letter |
| :----------: | :----: | :----: | :---: | :---: | :-----: | :----: |
| tex | *positions, socials* | - | *location, item* | *location* | *text* | *section, text* |
| darktext | *positions, socials* | - | *location, item* | *location* | *text* | *section, text* |
| graytext | - | - | *position, date* | *title, date* | - | *recipient, date, enclosure* |
| lighttext | - | *left, center, right* | - | - | - | - |
| highlight | *name, socials* | - | - | - | *photo, titles* | - |
