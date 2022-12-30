libnoise
========

This is a fork of libnoise which changes the build system to cmake.
It contains noiseutils and examples inside.
The building and installing is ONLY tested on Windows.

For more information see https://libnoise.sourceforge.net/index.html 

build and install
-----------------

Just cmake it.
Then open generated Visual Studio solution, build the Install project.

usage
-----

in your own CMakelists.txt
  
  project(myproj)
  
  find_package(noise 1 REQUIRED NO_MODULE)
  #it will report an error for not finding noiseConfig.cmake
  #set the noise_DIR to the directory, "build/install/lib/cmake/noise" by default, then reconfig it

  target_link_libraries(my_target PRIVATE noise::noise noise::noiseutils)
