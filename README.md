# SpriteSheetPacker

Sprite Sheet Packer is a fully featured tool for combining multiple individual images into a single, efficiently laid out image.

![](https://github.com/nickgravelyn/spritesheetpacker/blob/master/images/ToolUI.png|alt=Tool UI)

Sprite Sheet Packer supports reading PNG, JPG, BMP, and GIF images and produces a single PNG image with all the images embedded inside of it. The resulting image is transparent anywhere an image is not drawn. The tool also produces an accompanying file that maps the image file names with their rectangles, for use in your program to find the regions of the image you are interested in.

The tool has a full UI including options for setting the maximum resulting image size, padding (added to the size of the individual images), as well as options for requiring a power-of-two sized output and a square output. The tool has buttons for managing the desired images and also accepts drag-and-drop of image files into the list for true ease of use.

The build process is completely multithreaded to ensure smooth operation of the application even when processing large numbers of images.

The tool now supports plugins so you can create your own image or map file types without having to edit the application. Once you've compiled a DLL with your types in it, simply place it next to the exe and run the application. When you are choosing your image or map file location, use the drop down to choose the file type. For an example, see the XNA XML exporter in the source tree which exports an XML file in XNA Content format instead of the standard text file. The XNA XML exporter is also included, in compiled form, with the regular download.

Here are some sample output files created from 720 individual images found here: http://blogoscoped.com/archive/2006-08-08-n51.html using various combinations of the "Require Power of Two Output" and "Require Square Output" options:

Non-power of two and non-square:
![](https://github.com/nickgravelyn/spritesheetpacker/blob/master/images/Sheet1.png|alt=Sheet1)

Power of two and non-square:
![](https://github.com/nickgravelyn/spritesheetpacker/blob/master/images/Sheet2.png|alt=Sheet2)

Non-power of two and square:
![](https://github.com/nickgravelyn/spritesheetpacker/blob/master/images/Sheet3.png|alt=Sheet3)

Power of two and square:
![](https://github.com/nickgravelyn/spritesheetpacker/blob/master/images/Sheet4.png|alt=Sheet4)

Compiled binaries can be found in the Downloads section and the full source code is available in the Source Code section.

For an example of parsing the text output with XNA Game Studio, see Using Sprite Sheet Packer with XNA GS.

All code was written by Nick Gravelyn except the code for computing the efficient placement of the rectangles which was taken from the [Nuclex Framework](http://nuclexframework.codeplex.com/).
