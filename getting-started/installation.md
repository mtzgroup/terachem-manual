# Installation

First, obtain and install the latest CUDA driver (TeraChem 1.9 requires 352.93 or later). These can be obtained free of charge at

```
http://www.nvidia.com/drivers
```

Installation of the CUDA driver must be performed by a user with “root” permission, i.e. the superuser. Check with your local system administrator first, or type

```
cat /proc/driver/nvidia/version
```

since adequate CUDA drivers may already be installed. Make sure you select the 64-bit Linux operating system. After downloading the driver package, shut down the X server by typing

```
sudo init 3
```

Then launch the driver binary, and follow the instructions.

Previous versions of TeraChem (1.5K and earlier) required user installation of the CUDA toolkit. This is no longer required, as all the needed libraries are distributed with TeraChem. You do need to set the LD\_LIBRARY\_PATH environment variable correctly:

```
export LD_LIBRARY_PATH=$TeraChem/lib:$LD_LIBRARY_PATH
```

where you should replace $TeraChem with the path to your TeraChem installation.

To install the TeraChem software, first unpack the tc1.9.tar archive using the following command (in a temporary directory which you may later remove):

```
tar xvf tc1.9.tar
```

This will create a subdirectory TCInstaller. Run the install script by typing

```
cd TCInstaller
chmod u+x install
./install
```
