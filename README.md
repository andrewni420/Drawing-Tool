# Drawing-Tool
Final Project for Intro to Computer Science class. Loosely inspired by ChemDraw and LaTeX's asymptote package.

####### Instructions ######
 - Hover over the toolbar to see tooltips
 - Click on a tool to use it
 - Click inside the drawing pad to begin drawing
 - Drawing tools will automatically snap to a nearby object or its start/stop nodes. Hold Ctrl to suppress snap.

 - Ways to abort drawing:
 - Clicking on a tool will abort and select that tool
 - Clicking (or pressing enter) outside of the pad
 - Hotkeys

## Tool Descriptions ##
 - Marquee
    The nearest object to the mouse will be highlighted. 
    Click to select highlighted object.
    Shift + Click for additive selection
    Click on a selected object to unselect it
    
    All relevant nodes for selected objects will be shown in teal. Click and drag nodes to edit objects
    Click and drag a selected object to move all selected objects
    Click and drag an unselected object to clear selection, select it, and move it.
    Press delete to delete selected objects
    Click while no objects are highlighted to deselect everything
    
- Node
  Draw a point
  
- Line
  Draw a straight line

- Ellipse
  Draw an ellipse, a circle, or an arc

- Spline
  Draw a bezier spline
  https://en.wikipedia.org/wiki/B%C3%A9zier_curve

- Print
  Converts drawing into Asymptote code for LaTeX
  
- Open
  Opens an instructions text file as drawing
  
- Save
  Saves drawing as instructions
  
- Exit
  Exits application

## Use Cases ##
To draw a line from point 1 to point 2:
    1. Select line tool
    2. Click on point 1
    3. Click on point 2
    
To draw a circle with diametrically opposite points 1 and 2: 
    1. Select ellipse tool
    2. Click on point 1
    3. Click on point 2
    4. Press Enter
    5. Press Enter

To draw a circular arc:
    1. Find diametrically opposite points 1 and 2 to define the circle
    2. Select ellipse tool
    3. Click on point 1
    4. Click on point 2
    5. Press Enter
    6. Click on beginning of arc
    7. Click on end of arc
    When defining an arc, do not make the end coincide with the beginning.

To draw a spline from point 1 to point 2 using a set of predefined control points:
    1. Select spline tool
    2. Click on point 1
    3. Click on each control point 
    4. Press Enter with the mouse over point 2

To draw a spline from point 1 to point 4 with control points 2 and 3:
    1. Select spline tool
    2. Click on point 1
    3. Four options here:
        Click on point 2, Click on point 3, Press Enter on point 4
        Click on point 2, Ctrl+Click on point 4, Press Enter on point 3
        Ctrl+Click on point 4, Ctrl+Click on point 3, Press Enter on point 2
        Ctrl+Click on point 4, Click on point 2, Press Enter on point 3
       Ctrl is used to set spline points in reverse

To open/save as text file:
  Follow the prompt. Do not include the full path; just the name.
	Format for save files:
        	The first line is one integer - the number of objects. Data for objects follows.
        	For each object, the first line gives the type of object and number of nodes
        	Each node is a separate line, with x and y coordinates.
        	Ellipses have a third line giving semi major axis and endpoints
          
To save as image:
   Screenshot

## Hotkeys: ##
Space       =  marquee
1           =  node
2           =  line
3           =  ellipse
4           =  spline
Ctrl + P    =  print
Ctrl + S    =  save as
Ctrl + O    =  open file
Ctrl + A    =  select all
Esc         =  exit
	
## Known Bugs and Warnings ##
 - Sometimes snapping doesn't behave correctly. Usually restarting the program corrects this.
 - Only select and move one node at a time (i.e. do not shift+click while editing 		
   objects)
 - Don't move ellipse foci more than 2*a (semi major axis) away from each other
 - Don't superimpose endpoints for lines, splines, and arcs

