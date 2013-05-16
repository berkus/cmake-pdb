What our build process looks like:

 1) Build lib solution
 2) Copy outerlib.lib, outerlib.sln to exe folder
 3) Clean lib solution (to make sure all pdb files are gone)
 4) Build exe solution
