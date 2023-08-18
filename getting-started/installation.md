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

This script will verify that your machine has a suitable graphics card, verify that you accept the license terms, and install the software in a location of your choosing (the “TeraChem installation directory” or instdir in the following). The script will create SetTCVars.sh which sets the appropriate environment variables. You can add source $TeraChem/SetTCVars.sh to your shell configuration file (which is $HOME/.bashrc if you use the bash shell) to automatically configure the TeraChem environment at every new login session. The install script will also put a temporary license file in place so you can begin using TeraChem immediately. However, this temporary license file is time-limited, so you will want to obtain a permanent license file. The install script ends with a form suitable for emailing to help@petachem.com:

```
-------------BEGIN HERE------------------
Institution: ______________________
Ordered By: _______________________
MAC: 003048DB1D7E
IP: 171.64.125.189
---------------END HERE------------------
```

You can regenerate this at any time by typing

```
$TeraChem/bin/machid
```

Fill in the “Institution” and “Ordered By” fields and email to help@petachem.com. When we receive this from you, we will send you a permanent license file (which should be saved as license.dat in the TeraChem installation directory) within a few days. The TeraChem environment variable indicates where the licensing file can be found, i.e. $TeraChem/license.dat.
