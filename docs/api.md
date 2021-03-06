<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [setContextToDisplayFontSize][1]
-   [triggerEvent][2]
-   [convertToVector3][3]
-   [makeUnselectable][4]
-   [playClip][5]
-   [playClip][6]
-   [stopClip][7]
-   [stopClip][8]
-   [getPlayClipTimeouts][9]
-   [stopClipWithData][10]
-   [triggerStopEvent][11]
-   [createNewMeasurement][12]
-   [pointNearTool][13]
-   [pointNearHandle][14]
-   [pointNearHandleAllTools][15]
-   [mouseDownActivateCallback][16]
-   [startDrawing][17]
-   [addPointPencilMode][18]
-   [addPoint][19]
-   [endDrawing][20]
-   [mouseDownActive][21]
-   [mouseDownCallback][22]
-   [mouseDownCallback][23]
-   [mouseDownCallback][24]
-   [mouseMoveCallback][25]
-   [mouseMoveActive][26]
-   [checkInvalidHandleLocation][27]
-   [checkHandlesPencilMode][28]
-   [checkHandlesPolygonMode][29]
-   [invalidHandlePencilMode][30]
-   [mouseDragCallback][31]
-   [mouseUpCallback][32]
-   [mouseUpCallback][33]
-   [mouseDownPassive][34]
-   [modifyObject][35]
-   [modifyTextBox][36]
-   [modifyHandle][37]
-   [mouseHover][38]
-   [keyDownCallback][39]
-   [keyUpCallback][40]
-   [getMouseLocation][41]
-   [numberWithCommas][42]
-   [onImageRendered][43]
-   [enable][44]
-   [disable][45]
-   [activate][46]
-   [deactivate][47]
-   [removeEventListeners][48]
-   [getConfiguration][49]
-   [setConfiguration][50]
-   [dragObject][51]
-   [dragTextBox][52]
-   [dragHandle][53]
-   [dropObject][54]
-   [dropTextbox][55]
-   [dropHandle][56]
-   [toolName][57]
-   [toolName][58]
-   [insertOrDelete][59]
-   [deletePoint][60]
-   [insertPoint][61]
-   [getInsertionIndex][62]
-   [ClickedLineData][63]
-   [constructor][64]
-   [findLine][65]
-   [\_nearestHandleToPointAllTools][66]
-   [\_nearestHandleToPoint][67]
-   [\_getCloseLinesInTool][68]
-   [\_findCorrectLine][69]
-   [\_pointProjectsToLineSegment][70]
-   [\_getLineOriginToMouseAsVector][71]
-   [\_distanceOfPointfromLine][72]
-   [getCanvasPointsFromHandles][73]
-   [getLineAsVector][74]
-   [getNextHandleIndex][75]
-   [freeHandArea][76]
-   [calculateFreehandStatistics][77]
-   [getSum][78]
-   [sumPointIfInFreehand][79]
-   [pointInFreehand][80]
-   [isEnclosedY][81]
-   [isLineRightOfPoint][82]
-   [lineSegmentAtPoint][83]
-   [rayFromPointCrosssesLine][84]
-   [newHandle][85]
-   [newHandle][86]
-   [end][87]
-   [modify][88]
-   [doesIntersectOtherLines][89]
-   [doesIntersect][90]
-   [orientation][91]
-   [onSegment][92]
-   [FreehandHandleData][93]
-   [FreehandHandleData][94]
-   [dragCallback][95]
-   [dragCallback][96]
-   [createMagnificationCanvas][97]
-   [removeMagnificationCanvas][98]
-   [calculateMinMaxMean][99]
-   [applyWWWCRegion][100]
-   [recordStartPoint][101]
-   [getToolOptions][102]
-   [setToolOptions][103]
-   [clearToolOptions][104]
-   [clearToolOptionsByToolName][105]
-   [clearToolOptionsByToolType][106]
-   [clearToolOptionsByElement][107]

## setContextToDisplayFontSize

Sets the canvas context transformation matrix so it is scaled to show text
more cleanly even if the image is scaled up.  See
[https://github.com/cornerstonejs/cornerstoneTools/wiki/DrawingText][108]
for more information

**Parameters**

-   `enabledElement`  
-   `context`  
-   `fontSize`  

Returns **{fontSize: [number][109], lineHeight: [number][109], fontScale: [number][109]}** 

## triggerEvent

Trigger a CustomEvent

**Parameters**

-   `el` **EventTarget** The element or EventTarget to trigger the event upon
-   `type` **[String][110]** The event type name
-   `detail` **([Object][111] | null)** =null The event data to be sent (optional, default `null`)

Returns **[Boolean][112]** The return value is false if at least one event listener called preventDefault(). Otherwise it returns true.

## convertToVector3

Convert an Array to a cornerstoneMath.Vector3

**Parameters**

-   `arrayOrVector3` **([Array][113] | cornerstoneMath.Vector3)** Input array or Vector3

Returns **cornerstoneMath.Vector3** 

## makeUnselectable

A helper function to make an element (and its content) being non selectable.

**Parameters**

-   `element`  {HTMLElement} The element to make unselectable
-   `ignorePointerEvents`  {Boolean} true to make this element also ignore events
    (e.g. mouse click), false otherwise

Returns **void** 

## playClip

Starts playing a clip of different time series of the same image or adjusts the frame rate of an
already playing clip. framesPerSecond is optional and defaults to 30 if not specified. A negative
framesPerSecond will play the clip in reverse.
The element must have time series

**Parameters**

-   `element`  
-   `framesPerSecond`  

## playClip

Starts playing a clip or adjusts the frame rate of an already playing clip.  framesPerSecond is
optional and defaults to 30 if not specified.  A negative framesPerSecond will play the clip in reverse.
The element must be a stack of images

**Parameters**

-   `element`  
-   `framesPerSecond`  

## stopClip

Stops an already playing clip.

-   @param element

**Parameters**

-   `element`  

## stopClip

Stops an already playing clip.

-   @param element

**Parameters**

-   `element`  

## getPlayClipTimeouts

[private] Turns a Frame Time Vector (0018,1065) array into a normalized array of timeouts. Each element
... of the resulting array represents the amount of time each frame will remain on the screen.

**Parameters**

-   `vector` **[Array][113]** A Frame Time Vector (0018,1065) as specified in section C.7.6.5.1.2 of DICOM standard.
-   `speed` **[Number][109]** A speed factor which will be applied to each element of the resulting array.

Returns **[Array][113]** An array with timeouts for each animation frame.

## stopClipWithData

[private] Performs the heavy lifting of stopping an ongoing animation.

**Parameters**

-   `playClipData` **[Object][111]** The data from playClip that needs to be stopped.

Returns **any** void

## triggerStopEvent

[private] Trigger playClip tool stop event.

**Parameters**

-   `element`  

Returns **any** void

## createNewMeasurement

Initialises a new freehand data object

Returns **[Object][111]** measurementData - data object

## pointNearTool

Returns true if the mouse cursor is near a handle

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.
-   `toolIndex` **[Number][109]** the ID of the tool

Returns **[Boolean][112]** 

## pointNearHandle

Returns a handle of a particular tool if it is close to the mouse cursor

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.
-   `toolIndex` **[Number][109]** the ID of the tool

Returns **([Number][109] \| [Object][111] \| [Boolean][112])** 

## pointNearHandleAllTools

Returns a handle if it is close to the mouse cursor (all tools)

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.

Returns **[Object][111]** 

## mouseDownActivateCallback

Event handler for MOUSE_DOWN_ACTIVATE event, if tool is active and
the event is not caught by mouseDownCallback

**Parameters**

-   `e` **[Object][111]** The event.

## startDrawing

Begining of drawing loop when tool is active and a click event happens far
from existing handles.

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.

## addPointPencilMode

If in pencilMode, check the mouse position is farther than the minimum
distance between points, then add a point.

**Parameters**

-   `eventData` **[Object][111]** Data object associated with an event.
-   `dataHandles` **[Object][111]** Data object associated with the tool.

## addPoint

Adds a point on mouse click in polygon mode.

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.

## endDrawing

Ends the active drawing loop and completes the polygon.

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.
-   `handleNearby` **[Object][111]** the handle nearest to the mouse cursor.

## mouseDownActive

If in pencilMode, check the mouse position is farther than the minimum
distance between points, then add a point.

**Parameters**

-   `e`  
-   `toolData`  
-   `currentTool`  
-   `eventData` **[Object][111]** data object associated with an event.
-   `dataHandles` **[Object][111]** data object associated with the tool.

## mouseDownCallback

Event handler for MOUSE_DOWN event.

**Parameters**

-   `e` **[Object][111]** The event.

## mouseDownCallback

Draw the magnifying glass on mouseDown, and begin tracking mouse movements

**Parameters**

-   `e`  

## mouseDownCallback

Records the start point and attaches the drag event handler

**Parameters**

-   `e`  

## mouseMoveCallback

Event handler for MOUSE_MOVE event.

**Parameters**

-   `e` **[Object][111]** The event.

## mouseMoveActive

Event handler called by mouseMoveCallback when the tool is currently active.

**Parameters**

-   `eventData` **[Object][111]** data object associated with an event.
-   `toolData` **[Object][111]** data object associated with the freehand tool.

## checkInvalidHandleLocation

Returns true if the proposed location of a new handle is invalid.

**Parameters**

-   `data` **[Object][111]** data object associated with the tool.

Returns **[Boolean][112]** 

## checkHandlesPencilMode

Returns true if the proposed location of a new handle is invalid (in pencilMode).

**Parameters**

-   `data` **[Object][111]** data object associated with the tool.

Returns **[Boolean][112]** 

## checkHandlesPolygonMode

Returns true if the proposed location of a new handle is invalid (in polygon mode).

**Parameters**

-   `data` **[Object][111]** data object associated with the tool.

Returns **[Boolean][112]** 

## invalidHandlePencilMode

Returns true if the mouse position is far enough from previous points (in pencilMode).

**Parameters**

-   `data` **[Object][111]** data object associated with the tool.
-   `mousePoint` **[Object][111]** the position of the mouse cursor.

Returns **[Boolean][112]** 

## mouseDragCallback

Event handler for MOUSE_DRAG event.

**Parameters**

-   `e` **[Object][111]** The event.

## mouseUpCallback

Event handler for MOUSE_UP event.

**Parameters**

-   `e` **[Object][111]** The event.

## mouseUpCallback

Remove the magnifying glass when the mouse event ends

**Parameters**

-   `e`  

## mouseDownPassive

Event handler called by mouseDownCallback when the tool is currently deactive.

**Parameters**

-   `e` **[Object][111]** The event.

## modifyObject

Event handler called by mouseDownPassive which modifies a tool's data.

**Parameters**

-   `e` **[Object][111]** The event.
-   `nearby` **[Object][111]** Object containing information about a nearby handle.

## modifyTextBox

Event handler called by mouseDownPassive which modifies a tool's textBox.

**Parameters**

-   `element` **[Object][111]** The element associated with the event.
-   `nearby` **[Object][111]** Object containing information about a nearby handle.

## modifyHandle

Event handler called by mouseDownPassive which modifies a tool's handle.

**Parameters**

-   `element` **[Object][111]** The element associated with the event.
-   `nearby` **[Object][111]** Object containing information about a nearby handle.
-   `toolData` **[Object][111]** The data associated with the tool.

## mouseHover

Activates a particular tool when the mouseCursor is near one if it's handles
or it's textBox.

**Parameters**

-   `eventData` **[Object][111]** The data assoicated with the event.
-   `toolData` **[Object][111]** The data associated with the tool.

## keyDownCallback

Event handler for KEY_DOWN event.

**Parameters**

-   `e` **[Object][111]** The event.

## keyUpCallback

Event handler for KEY_UP event.

**Parameters**

-   `e` **[Object][111]** The event.

## getMouseLocation

Gets the current mouse location and stores it in the configuration object.

**Parameters**

-   `eventData` **[Object][111]** The data assoicated with the event.

## numberWithCommas

Adds commas as thousand seperators to a Number to increase readability.

**Parameters**

-   `number` **([Number][109] \| [String][110])** A Number or String literal representing a number.

Returns **[String][110]** A string literal representaton of the number with commas seperating the thousands.

## onImageRendered

Event handler for IMAGE_RENDERED event.

**Parameters**

-   `e` **[Object][111]** The event.

## enable

Attaches event listeners to the element such that is is visible.

**Parameters**

-   `element` **[Object][111]** The viewport element to attach event listeners to.

## disable

Disables the reference line tool for the given element.

**Parameters**

-   `element` **[Object][111]** The viewport element to attach event listeners to.

## activate

Attaches event listeners to the element such that is is visible, modifiable, and new data can be created.

**Parameters**

-   `element` **[Object][111]** The viewport element to attach event listeners to.
-   `mouseButtonMask`  

## deactivate

Attaches event listeners to the element such that is is visible and modifiable.

**Parameters**

-   `element` **[Object][111]** The viewport element to attach event listeners to.
-   `mouseButtonMask`  

## removeEventListeners

Removes event listeners from the element.

**Parameters**

-   `element` **[Object][111]** The viewport element to remove event listeners from.

## getConfiguration

Get the configuation object for the freehand tool.

Returns **[Object][111]** configuration - The freehand tool's configuration object.

## setConfiguration

Set the configuation object for the freehand tool.

**Parameters**

-   `config` **[Object][111]** The configuration object to set the freehand tool's configuration.

## 

Moves a part of the freehand tool whilst it is dragged by the mouse.

**Parameters**

-   `currentHandle` **[Object][111]** The handle being dragged.
-   `data` **[Object][111]** The data associated with the freehand tool being modified.

## dragObject

**Parameters**

-   `currentHandle`  
-   `data`  

**Meta**

-   **author**: JamesAPetts

## dragTextBox

Moves a freehand tool's textBox whilst it is dragged by the mouse.

**Parameters**

-   `currentHandle` **[Object][111]** The handle being dragged.

## dragHandle

Moves a handle of the freehand tool whilst it is dragged by the mouse.

**Parameters**

-   `currentHandle` **[Object][111]** The handle being dragged.
-   `data` **[Object][111]** The data associated with the freehand tool being modified.

## 

Places part of the freehand tool when the mouse button is released.

**Parameters**

-   `e` **[Object][111]** The event.
-   `toolData` **[Object][111]** The data associated with the freehand tool.

## dropObject

**Parameters**

-   `e`  
-   `toolData`  

**Meta**

-   **author**: JamesAPetts

## dropTextbox

Places a freehand tool's textBox.

**Parameters**

-   `eventData` **[Object][111]** Data object associated with the event.
-   `toolData` **[Object][111]** The data associated with the freehand tool.

## dropHandle

Places a handle of the freehand tool if the new location is valid.
If the new location is invalid the handle snaps back to its previous position.

**Parameters**

-   `eventData` **[Object][111]** Data object associated with the event.
-   `toolData` **[Object][111]** The data associated with the freehand tool.

## toolName

Type: [string][110]

**Meta**

-   **author**: JamesAPetts

## toolName

Type: [string][110]

**Meta**

-   **author**: JamesAPetts

## insertOrDelete

Inserts or deletes a point from a freehand tool.

**Parameters**

-   `e` **[Object][111]** The event.
-   `nearby` **[Object][111]** Object containing information about a nearby handle.

## deletePoint

Deletes a point from a freehand tool.

**Parameters**

-   `eventData` **[Object][111]** The data object associated with the event.
-   `deleteInfo` **[Object][111]** Object containing information about which point to delete.

## insertPoint

Inserts a new point into a freehand tool.

**Parameters**

-   `eventData` **[Object][111]** The data object associated with the event.
-   `insertInfo` **[Object][111]** Object containing information about where to insert the point.

## getInsertionIndex

Gets the handle index of a tool in which to insert the new point.

**Parameters**

-   `insertInfo` **[Object][111]** Object containing information about where to insert the point.

## ClickedLineData

Type: [Object][111]

**Properties**

-   `toolIndex` **[Number][109]** ID of the tool that the line corresponds to.
-   `handleIndexArray` **[Object][111]** An array of the handle indicies that correspond to the line segment.

## constructor

Constructs a linefinder with the eventdata

**Parameters**

-   `eventData` **[Object][111]** Data object associated with the event.

## findLine

Looks for lines near the mouse cursor.

Returns **[ClickedLineData][114]** 

## \_nearestHandleToPointAllTools

Finds the nearest handle to the mouse cursor for all tools.

Returns **[Object][111]** closestHandle - The handle closest to the point.

## \_nearestHandleToPoint

Finds the nearest handle to the mouse cursor for a specific tool.

**Parameters**

-   `toolIndex` **[Number][109]** The index of the particular freehand tool.

Returns **[Object][111]** An object containing information about the closest handle.

## \_getCloseLinesInTool

Finds all the lines close to the mouse point for a particular tool.

**Parameters**

-   `toolIndex` **[Number][109]** The index of the particular freehand tool.

Returns **[Object][111]** An array of lines close to the mouse point.

## \_findCorrectLine

Finds the line the user clicked on from an array of close lines.

**Parameters**

-   `toolIndex` **[Number][109]** The index of the particular freehand tool.
-   `closeLines` **[Object][111]** An array of lines close to the mouse point.

Returns **([ClickedLineData][114] | null)** An instance of ClickedLineData containing information about the line, or null if no line is correct.

## \_pointProjectsToLineSegment

Returns true if the mouse point projects onto the line segment.

**Parameters**

-   `toolIndex` **[Number][109]** The index of the particular freehand tool.
-   `handleIndexArray` **[Object][111]** An array of indicies corresponding to the line segment.

Returns **[Boolean][112]** True if the mouse point projects onto the line segment

## \_getLineOriginToMouseAsVector

Constructs a vector from the direction and magnitude of the line from the the line origin to the mouse cursor.

**Parameters**

-   `p` **[Object][111]** An array of two points respresenting the line segment.

Returns **[Object][111]** An array containing the x and y components of the vector.

## \_distanceOfPointfromLine

Calculates the perpendicular distance of the mouse cursor from a line segment.

**Parameters**

-   `handle1` **[FreehandHandleData][115]** The first handle.
-   `handle2` **[FreehandHandleData][115]** The first handle.

Returns **[Number][109]** The perpendicular distance of the mouse cursor from the line segment.

## getCanvasPointsFromHandles

Returns the canvas positions from the handle's pixel positions.

**Parameters**

-   `handle1` **[FreehandHandleData][115]** The first handle.
-   `handle2` **[FreehandHandleData][115]** The second handle.
-   `element` **[Object][111]** The element on which the handles reside.

Returns **[Object][111]** An array contsining the handle positions in canvas coordinates.

## getLineAsVector

Converts a line segment to a vector.

**Parameters**

-   `p` **[Object][111]** An array of two points respresenting the line segment.

Returns **[Object][111]** An array containing the x and y components of the vector, as well as a magnitude property.

## getNextHandleIndex

Gets the next handl index from a cyclical array of points.

**Parameters**

-   `currentIndex` **[Number][109]** The current index.
-   `length` **[Number][109]** The number of handles in the polygon.

Returns **[Number][109]** The index of the next handle.

## freeHandArea

**Parameters**

-   `dataHandles`  
-   `scaling`  

**Meta**

-   **author**: JamesAPetts

## 

Calculates the statistics of all the points within the freehand object.

**Parameters**

-   `sp` **[Object][111]** An array of the pixel data.
-   `boundingBox` **[Object][111]** Rectangular box enclosing the polygon.
-   `dataHandles` **[Object][111]** Data object associated with the tool.

Returns **[Object][111]** statisticsObj - Object containing the derived statistics.

## calculateFreehandStatistics

**Parameters**

-   `sp`  
-   `boundingBox`  
-   `dataHandles`  

**Meta**

-   **author**: JamesAPetts

## getSum

Calculates the sum, squared sum and count of all pixels within the polygon.

**Parameters**

-   `sp` **[Object][111]** An array of the pixel data.
-   `boundingBox` **[Object][111]** Rectangular box enclosing the polygon.
-   `dataHandles` **[Object][111]** Data object associated with the tool.

Returns **[Object][111]** sum - Object containing the sum, squared sum and pixel count.

## sumPointIfInFreehand

Adds the pixel to the workingSum if it is within the polygon.

**Parameters**

-   `dataHandles` **[Object][111]** Data object associated with the tool.
-   `point` **[Object][111]** The pixel coordinates.
-   `workingSum` **[Object][111]** The working sum, squared sum and pixel count.
-   `pixelValue` **[Object][111]** The pixel value.

## pointInFreehand

Calculates if "point" is inside the polygon defined by dataHandles by counting
the number of times a ray originating from "point" crosses the edges of the
polygon. Odd === inside, Even === outside. The bool "inROI" flips every time
the ray originating from location and pointing to the right crosses a
linesegment.

**Parameters**

-   `dataHandles`  
-   `location`  

**Meta**

-   **author**: JamesAPetts

## isEnclosedY

Returns true if the y-position yp is enclosed within y-positions y1 and y2.

**Parameters**

-   `yp` **[Number][109]** The y position of point p.
-   `y1` **[Number][109]** The y position of point 1.
-   `y2` **[Number][109]** The y position of point 2.

Returns **[Boolean][112]** True if the y-position yp is enclosed within y-positions y1 and y2.

## isLineRightOfPoint

Returns true if the line segment is to the right of the point.

**Parameters**

-   `point` **[Object][111]** The point being queried.
-   `lp1` **[Object][111]** The first point of the line segment.
-   `lp2` **[Object][111]** The second point of the line segment.

Returns **[Boolean][112]** True if the line is to the right of the point.

## lineSegmentAtPoint

Returns the y value of the line segment at the x value of the point.

**Parameters**

-   `point` **[Object][111]** The point being queried.
-   `lp1` **[Object][111]** The first point of the line segment.
-   `lp2` **[Object][111]** The second point of the line segment.

Returns **[Object][111]** An object containing the y value as well as the gradient of the line segment.

## rayFromPointCrosssesLine

Returns true if a rightwards ray originating from the point crosses the line defined by handleI and handleJ.

**Parameters**

-   `point` **[Object][111]** The point being queried.
-   `handleI` **[Object][111]** The first handle of the line segment.
-   `handleJ` **[Object][111]** The second handle of the line segment.

Returns **[Boolean][112]** True if a rightwards ray originating from the point crosses the line defined by handleI and handleJ.

## newHandle

Orientation algoritm to determine if two lines cross.
Credit and details: geeksforgeeks.org/check-if-two-given-line-segments-intersect/

**Parameters**

-   `candidateHandle`  
-   `dataHandles`  

**Meta**

-   **author**: JamesAPetts

## newHandle

Determines whether a new handle causes an intersection of the lines of the polygon.

**Parameters**

-   `candidateHandle` **[Object][111]** The new handle to check.
-   `dataHandles` **[Object][111]** data object associated with the tool.

Returns **[Boolean][112]** Whether the new line intersects with any other lines of the polygon.

## end

Checks if the last line of a polygon will intersect the other lines of the polgyon.

**Parameters**

-   `dataHandles` **[Object][111]** data object associated with the tool.

Returns **[Boolean][112]** Whether the last line intersects with any other lines of the polygon.

## modify

Checks whether the modification of a handle's position causes intersection of the lines of the polygon

**Parameters**

-   `dataHandles` **[Object][111]** data object associated with the tool.
-   `modifiedHandleId` **[Number][109]** The id of the handle being modified.

Returns **[Boolean][112]** Whether the modfication causes any intersections.

## doesIntersectOtherLines

Checks whether the line (p1,q1) intersects any of the other lines in the polygon.

**Parameters**

-   `dataHandles` **[Object][111]** data object associated with the tool.
-   `p1` **[Object][111]** Coordinates of the start of the line.
-   `q1` **[Object][111]** Coordinates of the end of the line.
-   `ignoredHandleIds` **[Object][111]** Ids of handles to ignore (i.e. lines that share a vertex with the line being tested).

Returns **[Boolean][112]** Whether the line intersects any of the other lines in the polygon.

## doesIntersect

Checks whether the line (p1,q1) intersects the line (p2,q2) via an orientation algorithm.

**Parameters**

-   `p1` **[Object][111]** Coordinates of the start of the line 2.
-   `q1` **[Object][111]** Coordinates of the end of the line 2.
-   `p2`  
-   `q2`  

Returns **[Boolean][112]** Whether lines (p1,q1) and (p2,q2) intersect.

## orientation

Checks the orientation of 3 points.

**Parameters**

-   `p` **[Object][111]** First point.
-   `q` **[Object][111]** Second point.
-   `r` **[Object][111]** Third point.

Returns **[Number][109]** 0: Colinear, 1: Clockwise, 2: Anticlockwise

## onSegment

Checks if point q lines on the segment (p,r).

**Parameters**

-   `p` **[Object][111]** Point p.
-   `q` **[Object][111]** Point q.
-   `r` **[Object][111]** Point r.

Returns **[Boolean][112]** If q lies on line segment (p,r).

## FreehandHandleData

**Parameters**

-   `position`  
-   `highlight`   (optional, default `true`)
-   `active`   (optional, default `true`)

**Meta**

-   **author**: JamesAPetts

## FreehandHandleData

Type: [Object][111]

**Properties**

-   `x` **[Number][109]** The x position.
-   `y` **[Number][109]** The y position.
-   `highlight` **[Boolean][112]** Whether the handle should be rendered as the highlighted color.
-   `active` **[Boolean][112]** Whether the handle is active.
-   `lines` **[Object][111]** An array of lines associated with the handle.

## dragCallback

Drag callback is triggered by both the touch and mouse magnify tools

**Parameters**

-   `e`  

## dragCallback

Draws the rectangular region while the touch or mouse event drag occurs

**Parameters**

-   `e`  

## createMagnificationCanvas

Creates the magnifying glass canvas

**Parameters**

-   `element`  

## removeMagnificationCanvas

Find the magnifying glass canvas and remove it

**Parameters**

-   `element`  

## calculateMinMaxMean

Calculates the minimum, maximum, and mean value in the given pixel array

**Parameters**

-   `storedPixelLuminanceData`  
-   `globalMin`  
-   `globalMax`  

## applyWWWCRegion

Calculates the minimum and maximum value in the given pixel array

**Parameters**

-   `eventData`  

## recordStartPoint

Records the start point of the click or touch

**Parameters**

-   `eventData`  

## getToolOptions

Retrieve the options object associated with a particular toolName and element

**Parameters**

-   `toolName` **[string][110]** Tool name identifier of the target options object
-   `element` **[HTMLElement][116]** Element of the target options object

Returns **[Object][111]** Target options object (empty if not yet set)

## setToolOptions

Set the options object associated with a particular toolName and element

**Parameters**

-   `toolName` **[string][110]** Tool name identifier of the target options object
-   `element` **[HTMLElement][116]** Element of the target options object
-   `options` **[Object][111]** Options object to store at target

Returns **void** 

## clearToolOptions

Clear the options object associated with a particular toolName and element

**Parameters**

-   `toolName` **[string][110]** Tool name identifier of the target options object
-   `element` **[HTMLElement][116]** Element of the target options object

Returns **void** 

## clearToolOptionsByToolName

Clear the options objects associated with a particular toolName

**Parameters**

-   `toolName` **[string][110]** Tool type identifier of the target options objects

Returns **void** 

<!-- >>>>> TODO: deprecate -->
## clearToolOptionsByToolType

Clear the options objects associated with a particular toolType
Deprecation Notice: This method will be replaced by clearToolOptionsByToolName

**Parameters**

-   `toolType` **[string][110]** Tool type identifier of the target options objects

Returns **void** 

## clearToolOptionsByElement

Clear the options objects associated with a particular element

**Parameters**

-   `element` **[HTMLElement][116]** Element of the target options objects

Returns **void** 

[1]: #setcontexttodisplayfontsize

[2]: #triggerevent

[3]: #converttovector3

[4]: #makeunselectable

[5]: #playclip

[6]: #playclip-1

[7]: #stopclip

[8]: #stopclip-1

[9]: #getplaycliptimeouts

[10]: #stopclipwithdata

[11]: #triggerstopevent

[12]: #createnewmeasurement

[13]: #pointneartool

[14]: #pointnearhandle

[15]: #pointnearhandlealltools

[16]: #mousedownactivatecallback

[17]: #startdrawing

[18]: #addpointpencilmode

[19]: #addpoint

[20]: #enddrawing

[21]: #mousedownactive

[22]: #mousedowncallback

[23]: #mousedowncallback-1

[24]: #mousedowncallback-2

[25]: #mousemovecallback

[26]: #mousemoveactive

[27]: #checkinvalidhandlelocation

[28]: #checkhandlespencilmode

[29]: #checkhandlespolygonmode

[30]: #invalidhandlepencilmode

[31]: #mousedragcallback

[32]: #mouseupcallback

[33]: #mouseupcallback-1

[34]: #mousedownpassive

[35]: #modifyobject

[36]: #modifytextbox

[37]: #modifyhandle

[38]: #mousehover

[39]: #keydowncallback

[40]: #keyupcallback

[41]: #getmouselocation

[42]: #numberwithcommas

[43]: #onimagerendered

[44]: #enable

[45]: #disable

[46]: #activate

[47]: #deactivate

[48]: #removeeventlisteners

[49]: #getconfiguration

[50]: #setconfiguration

[51]: #dragobject

[52]: #dragtextbox

[53]: #draghandle

[54]: #dropobject

[55]: #droptextbox

[56]: #drophandle

[57]: #toolname

[58]: #toolname-1

[59]: #insertordelete

[60]: #deletepoint

[61]: #insertpoint

[62]: #getinsertionindex

[63]: #clickedlinedata

[64]: #constructor

[65]: #findline

[66]: #_nearesthandletopointalltools

[67]: #_nearesthandletopoint

[68]: #_getcloselinesintool

[69]: #_findcorrectline

[70]: #_pointprojectstolinesegment

[71]: #_getlineorigintomouseasvector

[72]: #_distanceofpointfromline

[73]: #getcanvaspointsfromhandles

[74]: #getlineasvector

[75]: #getnexthandleindex

[76]: #freehandarea

[77]: #calculatefreehandstatistics

[78]: #getsum

[79]: #sumpointifinfreehand

[80]: #pointinfreehand

[81]: #isenclosedy

[82]: #islinerightofpoint

[83]: #linesegmentatpoint

[84]: #rayfrompointcrosssesline

[85]: #newhandle

[86]: #newhandle-1

[87]: #end

[88]: #modify

[89]: #doesintersectotherlines

[90]: #doesintersect

[91]: #orientation

[92]: #onsegment

[93]: #freehandhandledata

[94]: #freehandhandledata-1

[95]: #dragcallback

[96]: #dragcallback-1

[97]: #createmagnificationcanvas

[98]: #removemagnificationcanvas

[99]: #calculateminmaxmean

[100]: #applywwwcregion

[101]: #recordstartpoint

[102]: #gettooloptions

[103]: #settooloptions

[104]: #cleartooloptions

[105]: #cleartooloptionsbytoolname

[106]: #cleartooloptionsbytooltype

[107]: #cleartooloptionsbyelement

[108]: https://github.com/cornerstonejs/cornerstoneTools/wiki/DrawingText

[109]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[110]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[111]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object

[112]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[113]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[114]: #clickedlinedata

[115]: #freehandhandledata

[116]: https://developer.mozilla.org/docs/Web/HTML/Element
