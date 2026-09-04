[![GitHub License](https://img.shields.io/github/license/mashape/apistatus?branch=master&label=License&logo=GitHub&logoColor=ffffff&labelColor=282828&color=informational&style=flat)]()  
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)  

# OmniToTikz 
![Static Badge](https://img.shields.io/badge/Version-0.3-blue)

OmniGraffle plug-in to export selection as a tikz graphic


Instructions for installation can be found on Omni's [website](https://omni-automation.com/omnigraffle/setup.html)

You may need to add some tikz libraries (```usetikzlibrary```) to your document. I've not run this in a bare document to compile the bare minimum list of libraries. I import a local tikzExtras.tex that loads a bunch of items.

## How to Use
* Select one or more items in drawing
* Select ```Export_tikz``` from the ```Automation``` menu
* Copy tikz code from the OmniGraffle Automation Console (Automation &rarr; Show Console) Code is enclosed by an ```adjustbox``` statement.

  
## What Works
* Exports all lines with color, opacity, weight, and arrows (straight and curved lines only)
* Exports all shapes with fill and stroke color and opacity, line weight, (rectangles and circles)
* Exports Text 
  * Some formatting (alignment, wrapping, font size)
  * Carriage returns are converted to tikz '\\\\'
  * Curly brackets are properly inserted

## What Doesn't Work
Lots of things but in particular:
* Bezier and Orthogonal lines
* Grouped graphics
* Ignores dashed line format - all lines are solid
* Shapes that are not rectangles or circles
* Shadows
* Imported graphic images
* Text
  * OmniGraffle API only provides the formatting of the first char. Therefore all text is formatted per the first char
  * Unicode chars are currently replaced with '-'. Additionally some chars like > and < are improperly displayed
  * If the first char has coloring, the color is ignored.
* Saving to a file

## Notes
I use Zed as my editor for this work. If you want to play with the code in Zed you'll want to add the following to your ```settings.json``` file to get javascript code coloring:
```
  "file_types": {
  "JavaScript": ["omnigrafflejs"],
  }
```

This work is based on the OmniGraffle 7 Omni [API](https://omni-automation.com/omnigraffle/OG-API.html#LineType)
