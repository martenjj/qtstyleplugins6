Qt Style Plugins for Qt 6
=========================

This is a port of the previous QtStylePlugins package, which
provided additional widget styles not included with the base Qt
installation, to Qt 6.  The style plugins were originally available
at https://code.qt.io/cgit/qt/qtstyleplugins.git and mirrored at
https://github.com/qt/qtstyleplugins, but were never updated to be
able to be built and used with Qt 6.

The styles provided are Cleanlooks, Motif, CDE and Plastique.  If GTK+2
libraries and include files are available then the GTK2 style can also
be built.  The BB10 style has not yet been ported.

Building requires CMake, and the project can be built from source and
then installed in the same way as any other CMake project.  In a
suitable build location, do:

     git clone https://github.com/martenjj/qtstyleplugins6.git
     cd qtstyleplugins6
     mkdir build
     cd build
     cmake ..
     make
     sudo make install

After the plugins are built and installed, you should be able to
select the style in your desktop environment's settings (in KDE Plasma
use System Settings - Appearance & Style - Colours & Themes -
Application Style).  You can also start a specific application from
the command line with an option such as "-style cleanlooks".


Problems?
---------

Please raise an issue on GitHub (at http://github.com/martenjj/qtstyleplugins6)
if there are any problems with installing or using this package.


Thank you for your interest!
----------------------------

Jonathan Marten, http://github.com/martenjj
