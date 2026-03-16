Netgen mesh generator

NETGEN is an automatic 3d tetrahedral mesh generator. It accepts input from constructive solid geometry (CSG) or boundary representation (BRep) from STL file format. The connection to a geometry kernel allows the handling of IGES and STEP files. NETGEN contains modules for mesh optimization and hierarchical mesh refinement. Netgen 6.x supports scripting via a Python interface. Netgen is open source based on the LGPL license. It is available for Unix/Linux, Windows, and OSX.

Find the Open Source Community on https://ngsolve.org
Support & Services: https://cerbsim.com

### How to build

Release mode:
```cmd
cmake "../src" -DCMAKE_INSTALL_PREFIX="BASEDIR/install" -DOpenCascade_DIR="C:/Program Files/OCCT/cmake" -DCMAKE_BUILD_TYPE="Release"
cmake --build . --config Release --target install
```

where:
- OpenCascade_DIR points to OCC folder with cmake files (I was using OCC v7.6.3 due it being the constraint from the GUI)
- CMAKE_BUILD_TYPE: Debug, Release. This was patched for debug mode to link to MultiThreadedDebugDLL and not yet in the official Netgen