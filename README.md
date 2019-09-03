# ASE Export Script
MCampagnini (http://code.google.com/p/ase-export-vmc/)

This is a fork from the original project by MCampagnini. The script has been upgraded to support Blender 2.78a and Blender 2.80 (check the Releases).

## Videos
* Blender 2.63a and ASE 2.01 (http://www.youtube.com/watch?v=63Wz0FoK2U0)
* Blender 2.59 old version (http://www.youtube.com/watch?v=ZPQW5x1rhAY&feature=channel&list=UL)

## Installation
* Download and extract the ASE Export Script.
* In Blender, File / User Preferences.
* Go to the Add-On Tab.
* Install Add-On, select the extracted python script.
* Click Save as Default to enable the script every time Blender loads (optional).

You will find a new export option in File / Export called Ascii Scene Export (.ase).  If you do not see the script in the export menu after following the installation instructions, open the Add-On tab and find the script under Import-Export: ASCII Scene Exporter.  Be sure that it is enabled by checking the box next to the add-on name.  Contact me on my website if you still have problems exporting.

## Mesh Requirements
* All non-collision geometries must be UV unwrapped.
* All non-collision meshes must have a material applied.

## Optional
* Mesh may have more than one material
* Mesh may have more than one UV texture and/or a lightmap texture.
* Mesh may be assigned as a collision object.
* Mesh may have more than one collision object to determine collision borders.
* Mesh may be assigned smoothing groups.

## Collision Objects
Assign a mesh as a collision object by prefixing each object name with UCX_NAME, where NAME can be anything you would like (case-insensitive).

## Smoothing Groups
Assign smoothing groups by edge selecting the border of the faces you want assigned to a smoothing group, press ctrl+e and mark sharp.  Any face group separated with sharp edges will be assigned a smoothing group.

## Vertex Painting
Apply vertex painting in Blender as normal, be sure that you have at least two uv texture slots.  This is not a technical limitation, but due to time constraints I left the vertex painting code inside of a conditional that requires two uv textures.  In order to view your vertex painting in UDK you will have to import and set up your materials correctly within UDK.
