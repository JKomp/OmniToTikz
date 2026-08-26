[![GitHub License](https://img.shields.io/github/license/mashape/apistatus?branch=master&label=License&logo=GitHub&logoColor=ffffff&labelColor=282828&color=informational&style=flat)]()  

# OmniToTikz 
![Static Badge](https://img.shields.io/badge/Version-0.1-blue)

Omnigraffle plug in to export selection as a tikz graphic


Instructions for installation can be found on Omni's [website](https://omni-automation.com/omnigraffle/setup.html)

## How to Use
* Select one or more items in drawing
* Select ```Export_tikz``` from the ```automation``` menu
* Copy tikz code from console

  
## What Works
* exports all lines with color, weight, and arrows (straight and curved lines only)
* exports all shapes (rectangles and circles)

## What Doesn't Work
* lines that end at other lines
* Bezier and Orthogonal lines
* Ignores dashed line format - all lines are solid
* shapes that are not rectangles or circles
* shape line weight, stroke color, fill color
* Text - the basic code is there but I use a lot of unicode characters and they generate tikz errors.
* Saving to a file

## Notes
I use Zed as my editor for this work. If you want to play with the code in Zed you'll want to add the following to your ```settings.json``` file to get javascript code coloring:
```
  "file_types": {
  "JavaScript": ["omnigrafflejs"],
  }
```
