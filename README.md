##### Introduction

This is a simple tool for converting Bruker ParaVision MRI data to the NIfTI file format. It includes both a drag-and-drop graphical interface (Bru2Nii) as well as a command line tool (Bru2). The compiled tools run on Windows, Linux and OSX without requiring any other files to be installed. The source code can be built using Lazarus without any other tools required. This project is inspired by the Perl script pvconv (http://pvconv.sourceforge.net).

##### Usage (Command Line)

Provide the name of the Bruker format 'acqp' or 'subject' file you wish to convert. For example 
 Bru2 c:\mydata\subject
 
##### Usage (Graphical Interface)

Drag and drop the Bruker 'acqp' or 'subject' file you wish to convert. 

![alt tag](https://github.com/neurolabusc/Bru2Nii/blob/master/gui.png)

##### Compile from Source

1.) You will want to install Lazarus (http://www.lazarus-ide.org). For Windows, download and run the unified installer. For Linux and OSX, you will want to install the lazarus, fpc and fpc-src packages.
2.) You can build these tools from the graphical interface. For example, launch Lazarus. Select Project/OpenProject and then choose project you wish to compile (for example Bru2Nii.lpr). Finally, choose the Run/Run command. 
3.) To compile the console version from the command line, run either one of these commands "fpc Bru2.lpr" or "lazbuild -B Bru2.lpr".
4.) To build the graphical version from the command line, run the command "lazbuild -B Bru2Nii.lpr".

##### Versions

5May2015 : 
 - Original Beta version
 - Need examples to support images with multiple echoes (e.g. separate volumes from T2+PD acquisition
 - Need to get examples for setting origin and rotation correctly
 
##### License

Being inspired by a Perl script we maintain the same license (http://dev.perl.org/licenses/) as the original pvconv project.

##### Links

 * [pvconv](http://pvconv.sourceforge.net) converts Bruker data to the older Analyze format (and therefore does not retain spatial orientation information). [github page](https://github.com/matthew-brett/pvconv)
 * [Bruker2Analyze](http://www.mccauslandcenter.sc.edu/mricro/mricro/bru2anz/) is another Bruker to Analyze conversion tool. 
 * [dsi-studio](http://dsi-studio.labsolver.org/Manual/Parse-DICOM) can extract diffusion directions from Bruker datasets.
 * [mriutil](http://www.pennstatehershey.org/web/nmrlab/resources/software/mriutil) can view Bruker images without needing to convert them.