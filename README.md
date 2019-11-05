This is a Windows command line utility for compiling the Digital Chroma 
Toolkit's help source files into the resources used by the Toolkit, and also 
into HTML files that can be displayed in a web browser. The format for the 
source files is described in the helpcomp.cpp source file.

This is written to be compiled using Visual Studio 2017. It should also be 
compilable on the Mac under Xcode, although I haven't tried it.

To use this without compiling it, go into the directory containing the Digital 
Chroma Toolkit source, as cloned from the digital-chroma-toolkit repo, which 
already contains the current version of the executable, and type:

    helpcomp helpsrc help helphtml

It should translate the existing files in the helpsrc directory into HTML 
fragments in the help directory, which get included as resources in the 
Toolkit executable, and full HTML files in the helphtml directory, which you 
can view in a web browser. The helphtml\index.html file lets you view the help 
pages individually, while helphtml\master.html gives you one huge page suitable 
for doing global searches.

Be aware, though, that some versions of Firefox won't follow links in local 
files unless you first go into about:config and set the 
security.fileuri.strict_origin_policy variable to false. There may be similar 
issues in other browsers.

Once the help files are compiled, you can build the entire Toolkit in Qt 
Creator. If you ever create, delete, or rename help files, you must run qmake 
before rebuilding the Toolkit.

Bug reports to: bugs@digitalchroma.com
