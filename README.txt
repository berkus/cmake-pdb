What our build process looks like:

1) Create a lib solution in _build_/_lib_
   $ mkdir _build_/_lib_ && cd _build_/_lib_
   $ cmake ../../lib
   $ devenv outerlib.sln

2) Build INSTALL target in VS to build and install the lib.

3) Install the PDB file manually. This mimicks the actual build process.

Copy ${CMAKE_BINARY_DIR}/${BUILD_TYPE}/outerlib.pdb to _build_/outerlib directory.

4) Clean the lib solution to remove PDB files. This mimicks the actual build process
   where executable linked in following steps is located on another machine.

5) Create exe solution in _build_/_exe_
   $ mkdir _build_/_exe_ && cd _build_/_exe_
   $ cmake ../../exe
   $ devenv exe.sln

5) Build exe solution

cl emits warnings about missing vc100.pdb or vc110.pdb that was generated for intermediate innerlib.

Probably /Fd specification for innerlib is wrong?
