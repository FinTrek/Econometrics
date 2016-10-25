# Econometrics
Michael Creel's graduate level econometrics notes, example code, and support programs
- to get just the notes, click on econometrics.pdf, and then on Download, at the upper R of the page, which will download only the pdf. Links in the pdf point to files here on github, and will open in your browser.
- to run the examples, see Setup, below. OR, use the econometrics.iso image:
- all of the materials are available on the econometrics.iso operating system image. This can be run using virtualization, and gives quick access to running all of the examples using Octave, R, Julia, etc., without the need to install anything. econometrics.iso (warning, it's about 1.5 GB) is available at http://pareto.uab.es/mcreel/Econometrics/econometrics.iso

## There are a couple of unusual thing about these notes:
- they are available in editable form (econometrics.lyx), so that you can modify them to suit your needs: see www.lyx.org. They are however copyrighted, so you should learn about the GPL before modifying and distributing them.
- they contain links that point to example programs using the Octave matrix programming language. Octave sometimes gets little respect as a language for econometrics, with allegations that it is slow compared to Matlab, etc. A couple of points:
 - for plain Octave, these allegations are true, in some respects at least
 -  Octave is free, and it runs on all popular operating systems
 - plain Octave is perfectly good for ordinary econometrics of the sort that most students and many researchers need to do
 - Octave can easily be linked to parallel matrix algebra libraries so that it uses all cores of a computer. Plain Octave doesn't do that by default.
 -  Octave can be compiled using proprietary compilers, if you have them.
 - it is easy to use C++ code for bottlenecks. For serious research work on computationally demanding problems, this step is fundamental
 - it is easy to use OpenMP or MPI to use Octave for parallel computing. This can have a great performance effect, and your code is free and portable.
 - taking all this into account, Octave can be a reasonable choice for doing econometrics
- There are examples for stuff like OLS, ML, etc., but there is also working (GPL'd) code for nonparametric methods, simulation-based estimation methods, estimation of DSGE models, and parallel programming applications in econometrics. The examples make use of some other code for GNU Octave that I have written - minimizers and other stuff, available here.
-the example programs together with data and all needed software are on the accompanying econometrics.iso image. This is an ISO image which can be used to boot a computer, but which is more easily used to boot a virtual computer, running under your usual operating system. This works with all of the popular operating systems. Using this method, you can be running the examples in very little time, without the hassle of installing a lot of software.
-You may be wondering why the notes are available in this form. It's simply because I use a lot of free software, and this is a means of contributing back to the community. Also, I'm hoping to receive error corrections and contributions from users of the notes.

- To run the examples, you need to have Octave installed. To edit the notes, you need to install LyX.
- econometrics.iso (about 1.3GB) contains the notes and all the examples, ready to run. You don't need to install anything to use it (except a virtualization platform, if you don't have one installed). I test the image using Virtualbox, which is a free download for Windows, MacOS, and Linux. There is an appliance econometrics.ova. To use the ISO image in a virtual machine, import the .ova appliance file into Virtualbox, then in Settings, make the Storage->IDE controller point to the location where you have save the econometrics.iso file.
Fixes for the live CD image: It seems I forgot to do a few things when preparing the image. To make everything work properly, do the following: open a terminal and type `cd ~; mkdir backup; cd Econometrics/MyOctaveFiles/OctFiles; make clean; make all`

# Setup
- to be able to run the examples, download the whole repo
- To prepare the software in this directory for use, you must have Octave installed. Octave v4.0 or more recent is recommended.
- For full functionality, you need to compile some things. If you are using this on your own Linux distro, open a terminal, and type "setup_econometrics" to prepare the software. You need to have the gcc compiler and build libraries installed for this to work. For Windows and OSX, I don't know the steps.
- the last step is to include the Econometrics directory in your Octave run path.



