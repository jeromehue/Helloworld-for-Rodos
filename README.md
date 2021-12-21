
First of all check that you are importing the correct rodos package in
`source/CMakeLists.txt `.

! Names and versions may vary and are given as an indication only.

To build for linux :
```
find_package(Rodos-stm32f4 0.1.0 REQUIRED)
```
To build for stm32f429
```
find_package(Rodos-stm32f4 0.1.0 REQUIRED)
```


To generate makefiles, run :
```shell
cmake -DCMAKE_TOOLCHAIN_FILE=/path/to/toolchain/file . -B build
```

Then cd into the build directory and make
```shell
cd build
make
```
