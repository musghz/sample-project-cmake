Compile using cmake
For Ubuntu desktop

Steps to compile and run this project:

-There should be 3 directories: build, include, src.
-Navigate to the build directory:
  $ cd build
-Run the cmake command from within the build directory:
  $ cmake ..
-A Makefile will be generated. Build the project using the make command:
  $ make
-After a successful build, run the executable:
  $ ./gaussianRandomV03cCpp
-Data for the gaussRand() and rand() functions will be printed to the terminal.
-Histograms based on these data will be stored in an html file.
-The html file will automatically launch in the default web browser.
