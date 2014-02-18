forceDirCoeffs_local-global
===========================

Modification of the forceCoeffs library for OpenFOAM to include force and moment coefficients in both global and local to the body coordinate systems.

The files are created for OpenFOAM 2.2.2 and based on the work of Wyldckat (see link below).  

https://github.com/wyldckat/forceDirCoeffs


A few steps...

1. Open a Terminal and follow these instructions to build from git.
 - cd to any directory you wish to install this library in.
 - git clone git://github.com/gxldesign/forceDirCoeffs_local-global.git
 - cd forceDirCoeffs
 - git checkout of22x
 - wmake libso forceDirCoeffs
2. Cut the file "forceDirCoeffs_LG" and Paste it in the case you are attemping to run in the "/system" folder.
3. This is now going to replace the "forceCoeffs" file that defines your parameters for force calculations.
4. Follow the instructions on the "How to use it" on Wyldckat's README.md page.
5. Enter your local and global coordinate vectors into the file "forceDirCoeffs_LG".  

Note: Once you have installed this library, if you wish to not use the local coordinate system, you will need to either revert in your "controlDict" file to the regular "forceCoeffs" library or enter an arbitrary local coordinate system into the file "forceDirCoeffs_LG".
