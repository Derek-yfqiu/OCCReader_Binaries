*******************************************************************************
OCCReader:
A plugin for visualizing CAD file in STEP,IGES and BREP format in ParaView.
*******************************************************************************

OCCReader is a ParaView plugin for importing CAD files in Open CASCADE (OCC)
open-source format STEP, IGES and BREP and visualizing in ParaView. This plugin
facetes CAD solids into VTK Polydata. With this plugin, the CAD geometry can be
visualized together with physical fields, so that the traditional way of using
STL file to visualizing geometry can be avoided. Three dispaly modes are
provided-- wireframe(mode 1), shading(mode 2) and wireframe+shading (mode 3).
The faceting accuracy can by increase by adjusting the "Deflection" parameter.
This document provides instrutions for compiling the plugin.


*******************************************************************************
Install the plugin in Linux system

-> Download a ParaView binary executable from www.paraview.org/download.
ATTENTION, the executable version should be consistent with the plugin
requirement. For example, plugin
"OCCReader_for_ParaView_4.3.1_Ubuntu_14.04_64bit" requires ParaView_4.3.1.

-> Unzip the ParaView bindary package, and also the OCCReader plugin file. Copy
all the files from OCCReader folder to the "lib" folder of ParaView binary. 

->You need to load this library manually for the first time. In ParaView menu
Tools->Manage Plugins, click "Load New" to load the "libOCCReader.so" in the
"lib" folder, and select "Auto Load" to load it automatically.


*******************************************************************************
Install the plugin in Windows system

 The approach used for Linux system is not workingdue to the problem of
 compiler compabitility. Therefore, the entire ParaView is distributed together
 with the plugin. Some reader and filter plugins are missing in this ParaView
 distribution.

-> Download the windows version of OCCReader plugin, which is a special ParaView
distribution. Unzip it, and open the paraview.exe.

->You need to load this library manually for the first time. In ParaView menu
Tools->Manage Plugins, click "Load New" to load the "OCCReader.dll" in the some
folder as paraview.exe , and select "Auto Load" to load it automatically.

********************************************************************************
********************  How to use this plugin ***********************************

This plugin is used like other ParaView Reader plugin. In ParaView, click "Open" 
button, you can find "OpenCASCADE CAD file(*.step,*.stp,*.igs,*.iges,*.brep)" in 
The draw-down list. If yes, you can import any CAD files in those formats. If not,
please make sure that the plugin is loaded correctly. 

-> Loading a CAD file, click "Apply" to process the model. 

-> Display mode is for setting the display effect:

	->mode 1: wireframe mode
	->mode 2: shading mode
	->mode 3: wireframe & shading

->Deflection is for adjusting the display precision. The smaller deflection means 
  smaller tolerance, thus higher precision. 

->After changing the parameters, click "Apply" to take effect. 



For any questions related to the use of this software/library you may contact
Ulrich Fischer(ulrich.fischer@kit.edu) or, for technical assistance, contact
Yuefeng Qiu (Yuefeng.qiu@kit.edu).
   
Have fun playing with it!   :)
   