What our build process looks like:

1) Create a lib solution in _build_/_lib_
   $ mkdir _build_/_lib_ && cd _build_/_lib_
   $ cmake ../../lib
   $ devenv outerlib.sln

2) Build INSTALL target in VS to build and install the lib.

3) Create exe solution in _build_/_exe_
   $ mkdir _build_/_exe_ && cd _build_/_exe_
   $ cmake ../../exe
   $ devenv exe.sln

4) Build exe solution
