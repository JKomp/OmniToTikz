[![GitHub License](https://img.shields.io/github/license/mashape/apistatus?branch=master&label=License&logo=GitHub&logoColor=ffffff&labelColor=282828&color=informational&style=flat)]()  
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)  

# OmniToTikz 
![Static Badge](https://img.shields.io/badge/Version-0.1-blue)

OmniGraffle plug-in to export selection as a tikz graphic


Instructions for installation can be found on Omni's [website](https://omni-automation.com/omnigraffle/setup.html)

## How to Use
* Select one or more items in drawing
* Select ```Export_tikz``` from the ```Automation``` menu
* Copy tikz code from the OmniGraffle Automation Console (Automation &rarr; Show Console)

  
## What Works
* Exports all lines with color, weight, and arrows (straight and curved lines only)
* Exports all shapes (rectangles and circles)

## What Doesn't Work
Lots of things but in particular:
* Lines that end at other lines
* Bezier and Orthogonal lines
* Ignores dashed line format - all lines are solid
* Shapes that are not rectangles or circles
* Shape line weight, stroke color, fill color
* Text - the basic code is there but I use a lot of unicode characters and they generate tikz errors.
* Saving to a file

## Notes
I use Zed as my editor for this work. If you want to play with the code in Zed you'll want to add the following to your ```settings.json``` file to get javascript code coloring:
```
  "file_types": {
  "JavaScript": ["omnigrafflejs"],
  }
```

This work is based on the OmniGraffle 7 Omni [API](https://omni-automation.com/omnigraffle/OG-API.html#LineType)
