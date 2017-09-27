This project makes use of the following packages:
gfortran
libglfw3-dev
freeglut3-dev
libglew-dev
libxmu-dev
libeigen3-dev
doxygen
subversion
libblas-dev liblapack-dev
libboost-all-dev
swig
ocl-icd-opencl-dev
fftw2

This list is formed by packages, how they appeared in APT Debian package manager, the names may be different on RedHat distributions. 

also cmake >= 3.0

gcc version must accept c++11. Currently, the project was tested with gcc 5.0 or higher.

git clone --recursive location for gchmc

cd gchmc/

cd gmolmodel/

mkdir build-debug

cd build-debug/

bash ../cmake_regenerateAll.sh && make -j4

for cmake_regenerateAll.sh you need root privileges since currently, all the libs are installed in /usr/local/lib ..

if you work into gmolmodel you only have to use make -j4 or cmake .. && make -j4 ( the second is in case you make changes into CMakeLists.txt )
in case you work into the other 2 projects you need to use : bash ../cmake_regenerateAll.sh  && make
Don't worry, it's not going to take as much as the first time :)

