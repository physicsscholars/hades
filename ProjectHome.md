# 1. Summary #
We freely release a software package <a href='http://hades.googlecode.com/files/HeartPhantomSoftware.zip'><b>Heart Phantom Development Software (Hades)</b></a> for an automatic heart phantom development purpose and freely distribute <a href='http://hades.googlecode.com/files/HeartPhantomDemos.zip'><b>two developed high-resolution heart phantoms</b></a> for the medical imaging research. HADES is developed in the <a href='http://www.fda.gov/MedicalDevices/DeviceRegulationandGuidance/GuidanceDocuments/ucm070277.htm>FDA<b>/</b'>Office of Science andEngineering Laboratories/Division of Imaging and Applied Mathematics</a>. Once the user defines a set of parameters and selects a Computed Tomography Angiography (CTA) data set, the software can generate segmented models of the heart envelope, muscle, coronaries and left ventricle automatically, and output the results as 3D renderings. The models can be saved either as volumetric data or as surface mesh data.

Currently, some digital heart phantoms, such as NCAT/XCAT phantoms, are available and have made important contributions to the field of medical image modeling. However, for most of the existing heart phantoms, the resolution is too low for realistic PTCA and CTA simulation and the coronary arteries are usually missing. To overcome the limitations of existing phantoms, this software presents a platform for building high resolution cardiac/coronary artery phantoms for imaging and dosimetry simulations. Since heart phantoms constructed with this software will be anatomically realistic, the associated pathology can also be modeled much more accurately and realistically. For example, different sized vessel stenoses can be synthesized and inserted at different locations in the coronary tree. In addition to the segmentation, the software provides a set of model manipulation tools, such as stenosis synthesis, volume addition and subtraction, mesh generation and skeleton extraction, so that the user can modify and analyze the model data easily. One can even model the detailed morphology of an atherosclerotic plaque in terms of its lipid core, surrounding matrix, and the overlying fibrous cap.

**This software was not designed nor is suitable for any clinical purposes.** Since this software is solely developed for research purposes, it is not guaranteed bug-free. The source code for the segmentation is available at [http://code.google.com/p/hades](http://code.google.com/p/hades). The license is an "Open Domain" license. The source code is free to download, for use or modification.

## Disclaimer ##
This software and documentation were developed at the Food and Drug Administration (FDA) by employees of the Federal Government in the course of their official duties. Pursuant to Title 17, Section 105 of the United States Code, this work is not subject to copyright protection and is in the public domain. FDA assumes no responsibility whatsoever for use by other parties of its source code, documentation or compiled executables, and makes no guarantees, expressed or implied, about its quality, reliability, or any other characteristic. Although this software can be redistributed and/or modified freely, we ask that any derivative works bear some notice that they are derived from it, and any modified versions bear some notice that they have been modified.

---


# 3. Installation and Configuration #
The code was developed using the following software in Linux Ubuntu 9.10: _VTK, ITK, QT_ and _CMAKE_. The recommended versions are as follows:

_VTK 5.2.1; VTK-Dev 5.2.1; ITK 3.2.1; ITK-Dev 3.2.1;_

_QT 4.5; QT-Dev 4.5; Qt-Designer 4.5; CMAKE 2.8;_

_libgdcm; libgdcm2-dev; libopenjpeg; libopenjpeg-dev; libinsighttoolkit3\_dev_

Newer versions of the toolkits and Ubuntu version are also usable. Since our software depends on VTK and ITK, the copyright information about VTK and ITK can be found in following links:

[http://www.itk.org/HTML/Copyright.htm](http://www.itk.org/HTML/Copyright.htm)

[http://www.vtk.org/VTK/project/license.html](http://www.vtk.org/VTK/project/license.html)

After installing these aforementioned software packages, the user can decompress the segmentation package into a directory provided that _CMakeList.txt_ is included in the same directory as the other source codes. Then, use _./SegBuild_  in shell to compile the segmentation program. The final output is the binary file: _**Segment**_, located in the current folder.


---


# 4. Segmentation Tools #

After the installation, the software can be run as shown in the following figure.

http://hades.googlecode.com/files/mainframe.PNG

Additionally, this package also provided a set of image processing method, such as volume cutting, volume adding and subtracting, large object selection, mesh-to-volume and volume-to-mesh conversion, skeleton extraction, longest vessel auto-selection, vesselness matrix calculation and so on. It will benefit more than heart phantom segmentation tasks. The following pictures show the capability of the platform. Please refer the [Readme file](http://code.google.com/p/hades/downloads/list)->"Tools" section for details.

http://hades.googlecode.com/files/tools3.JPG

# 5. Free High-resolution Heart Phantoms #
Currently, we provide [two high-resolution heart phantoms](http://hades.google.com/p/hades/downloads/list), One adult male and one adult female phantom, in this website (**HeartPhantomDemos.zip in the download page**). In each phantom, we provide a ventricle, a heart myocardium, both left and right coronary arteries and a set of arteries with pre-synthesized stenoses on it. Each group of stenoses are synthesized in the same location with different sizes. All the phantom data in this website are free to download and use.

Here we show an example of the heart phantom that we've developed. The mesh file of this phantom can be download from this website.

http://hades.googlecode.com/files/female1.JPG

Here we also illustrate the improved body phantoms with our high-resolution heart phantoms and some projections of different stenoses generated by Monte Carlo code to demonstrate the potential usage of our phantoms. You can download the entire Monte Carlo package for free in [the related project](http://code.google.com/p/penmesh/).

http://hades.googlecode.com/files/MonteCarlo.JPG


When using the phantoms, or the code, or the compiled software, please cite the following paper:

<a href='http://iopscience.iop.org/0031-9155/56/18/005'><b><i>S. Gu, R. Gupta and I. Kyprianou, Computational high-resolution heart phantoms for medical imaging and dosimetry simulations, Phys. Med. Biol., vol. 56, no. 18, pp. 5845-5864, 2011.</i></b></a>

## Acknowledgements ##
This project was supported in part by an appointment to the Research Participation Program at the Center for Devices and Radiological Health administered by the Oak Ridge Institute for Science and Education through an interagency agreement between the U.S. Department of Energy and the U.S. Food and Drug Administration. Special gratitude is expressed here for the help and recommendations of Dr. Aldo Badano, Dr. Kyle Myers, Dr.
Andreu Badal-Soler, Dr. Camille Vidal, Mr. Samir Abboud. Dr. Rajiv Gupta (Ph.D and MD from Massachusetts General Hospital, Department of Radiology) provided us with the cardiac data sets to develop the software.

If you have any questions, please contact [iacovos.kyprianou@fda.hhs.gov] or [songxiang.gu@gmail.com]
