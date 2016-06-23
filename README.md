LCInterlocking
==========

Experimental module for FreeCAD 0.14.
It is not reliable, you have to check parts before doing the laser cut, don't trust it !

Video demonstration : https://youtu.be/YGFIdLpdWXE

Goal
--------------------
This experimental FreeCAD module is used to create interlocking laser cut parts.
For example, a box created by a conventional method of FreeCAD PartDesign. A first feature creates connections
between parts (simple tabs/holes or T-Slots).
A second feature rotate every pieces that belong to the same plane and uses the projection of the Draft module.
The contours of parts may be exported to svg format.
Then we must with SVG tool (inkscape or other) to delete some unnecessary lines before using it for laser cutting.

Interlocking
--------------------
Each involved part have to be configured (thickness, laser cut beam diameter...). Select part(s) by selected each entire
parts or just a face and click on "Add parts" or "Add same parts". The second button allows to share the same
properties between selected parts avoiding to set manually same properties for each part.
Then, select face(s), kind of join (tab, T-slot or continuous) and click on "Add face(s)" or "Add same faces". "Same
faces" is used to share same tab properties between selected faces.
Click on preview to view result on an other document. Click OK to create new parts in the current document.

SVG export
--------------------
Parts to be exported have to be selected before clicking to this feature. A new document is created with copied parts
and projections on XY plan. Select projections and export it to the Flattened SVG format. You can use inkscape to
remove some unwanted lines as line between tab and its parts. To do it, ungroup all, object to path, remove unwanted lines, join
curves with very little tolerance and you can regroup all if you want.

Some details are not correctly drawn with Inkscape (i.e. "circle) in contrary to Corel Draw for example.

TODO
----
 * Test with newer version of FreeCAD.
 * Add tolerance parameter.
 * ...