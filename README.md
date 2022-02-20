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
* `Shape` - Shape of the image (optional) (`circle`, `rectangle`)
* `Frame` -  Define whether the image is framed or not (optional) (`edge`, `noedge`)
* `Fill` -  Higlighte the image background with the `highlight` color (optional) (`fill`, `nofill`) !only works with png's or pdf's
* `Position` - Position of the image (optional) (`left`, `right`, `sidebar`) !left and right only works with centred header
* `Size` - Size of the image e.g. 2.5 cm
* `Image Path` Path where the image is stored e.g. pics/pp2.pdf

## Background
Set a background that is loaded on every page
```
\background[<Opacity>]{<Background Image Path>}
```
* `Opacity` Opacity of the background e.g. 0.15 (optional)
* `Background Image Path` Path to the background image e.g. pics/background5.pdf

## Header
In order to generate the header a number of optional arguments must first be specified

### Contact Information
```
\name{<Forename>}{<Surname>}
\address{<Adress>}
\mobile{<Mobile Number>}
\email{<Email Adress>}
\github{<Github ID>}
\linkedin{<Linkedin ID>}
\homepage{<Homepage URL>}
\twitter{<Twitter ID>}
\xing{<Xing ID>}
\stackoverflow{<SO ID>}{<SO Name>}
\skype{<Skype ID>}
\reddit{<Reddit ID>}
\extrainfo{<Some Info>}
```

### Further Information
```
\position{<Current or Last Position>}
\headwords{<A Few Words About Yourself>}
\quote{<Some Quote>}
```
### Make Header
In order to make the header one can now simply use the following command
```
\makecvheader[<Position>]
```
* `Position` Position of the header (`L` = left, `C` = right)<br/>
Attention! Only works after `\begin{document}`

## Sidebar
In order to generate the sidebar a number of optional arguments must first be specified
```
\aboutMe[<Section Title>]{<Content>}
\nonProfit{<Section Title>]{<Content>}
\userSection[<Section Title>]{<Content>}
```
* `Section Title` Section title (optional)

### Skills
```
\skillset[title/<Section Title>,label/<Label>]{<Label1/Grade1>,<Label2/Grade2>, ect.}
```
* `Section Title` Title of the skills section (optional)
* `Label` Label below the skill bars (optional)
* `Label/Grade` Skill and grade where the grade is a value from `0` to `1`<br/>
The number of skills is variable

### Languages
```
\languages[<Section Title>]{{<Language1/Level1>},{<Language2/Level2>}, ect.}
```
* `Section Title` Title of the languages section (optional)
* `Language/Level` Language and level e.g. German/Mother tongue

### Make Sidebar
In order to make the sidebar one can now simply use the following command
```
\makecvsidebar[xOffset/<xOffset>,yOffset/<yOffset>,<Corners>]
```
* `xOffset` Offset in x direction e.g xOffset/15pt
* `yOffset` Offset in y direction e.g yOffset/-15pt
* `Corners` Corner radius (`noRadius`, `radius`)<br/>
Attention! Only works after `\begin{document}`

## Footer
The footer can simply be defined using the following command
```
\makecvfooter(<Left Content>}{<Center Content>}{<Right Content>)
```
Attention! Only works after `\begin{document}`

## CV Entry

## Honors

## Cover Letter

## Multi Pages

