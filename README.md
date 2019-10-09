# Imagine-T3D-Importer
Blender import script for [Imagine](https://en.wikipedia.org/wiki/Imagine_(3D_modeling_software)) by Impulse, Inc. [.TDDD object file](http://www.ian.org/ImagineTDDDFormat.html) (aka 3D Data Description)

See also: [Imagine Staging Stage Editor File Format](istg.zip)

Thanks to Ken Nign (Ken9), the author of [LightWave](https://www.lightwave3d.com/) Object (.lwo) [importer](https://github.com/sftd/blender-addons/blob/master/io_import_scene_lwo.py), that inspired me a lot!

## Supported IFF chunks and sub-chunks

T3D files are organized as [IFF](https://en.wikipedia.org/wiki/Interchange_File_Format) chunks, the importer actually supports:
- 'OBJ ' (the first and only one chunk for TDDD describing the object heirarchy)
- DESC sub-chunk, describing one node of a heirarchy, and related TOBJ chunk marking the end of a heirarchy chain
- NAME, object name in the attributes requester
- POSI, the position (in world coordinates) 
- SIZE
- PNTS and PNT2, containing all the points of the object
- EDGE and EDG2, contains the edge list 
- FACE and FAC2, contains the triangle (face) list 
- COLR, REFL, TRAN, SPC1, the main object RGB color, and reflection, transmission and specularity coefficients
- PRP1, more object properties like hardness, roughness, shininess

![Screenshot](wizardgsz-u-and-i.jpg)

## Sample data
- [Aminet | 3dobj](http://aminet.net/pix/3dobj)
- [cd.textfiles.com](http://cd.textfiles.com/zoom2/graphics/raytracing/objects/)
- [CAD Technologies](http://www.imaginefa.com/objects.shtml)

