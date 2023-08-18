# System Requirements

This version of TeraChem was compiled and tested under 64-bit RedHat Enterprise Linux 6.6 operating system running on Intel Core2 quad-core and Intel Xeon 5520 dual quad-core CPU machines. An Nvidia compute capability 2.0 (Tesla C2050 or similar) or higher (i.e. Tesla K20 or similar) graphics card is required to run the program. Please refer to the CUDA Programming Guide at http://www.nvidia.com/object/cuda\_develop.html for the most current list of Nvidia GPU’s that meet this requirement. A CUDA driver (352.93 or later) must be installed on the system. If desired, v7.5 of the CUDA Toolkit may also be installed (but this is not necessary). Details on how to obtain and install the CUDA driver are provided below.

Because the binary file is linked against the Intel MKL library, it is recommended to run TeraChem on Intel-based workstations.

The amount of CPU RAM needed depends on the size of the molecules that will be studied. If the molecules of interest are relatively small (less than 500 atoms), the usual 8Gb or 16Gb configuration is acceptable. For very large molecules (in excess of 10,000 basis functions), CPU RAM will often be a limiting factor. For example, molecules with 25,000 basis functions require almost 70GB of CPU memory.
