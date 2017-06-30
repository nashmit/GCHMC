git clone --recursive <location for gchmc>
cd gchmc/
cd gmolmodel/
vim cmake_install_dep.sh
//change -DAnacondaEnvironmentPath="/home/osboxes/Anaconda/envs/" with your correct path to your envs's folder from your anaconda folder
// save :)
mkdir build-debug
cd build-debug/
bash ../cmake_install_dep.sh  && source activate mmtk_environment && bash ../cmake_cmake.sh && make

That's it, no environment variable :)
Enjoy! :)

p.s. : 2 libs are generated into build-debug/lib folder :)
P.S. P.S : the other 2 libs are generated into there build-debug folders  :) 

if you work into gmolmodel you only have to use make or bash ../cmake_cmake.sh && make  ( the second is in case you make changes into CMakeLists.txt )
in case you work into the other 2 projects you need to use : bash ../cmake_install_dep.sh  && source activate mmtk_environment && bash ../cmake_cmake.sh && make
Don't worry, it's not going to take as much as the first time :)

Also.. as you can see, it puts automatically mmtk_environment active.. so, when you work later, you have to be sure that you're using it before you start working :)

kind reminder :) Don't go away from your computer, you may have to introduce some passwords :)

also, I'm going to put a copy of my virtual machine on the ftp server.
if you wont to generate an Eclipse project from gmolmodel you can do that by setting a variable into cmake command into cmake_cmake.sh script
