# Environment Variables

There are several environment variables that influence TeraChem:

* **TeraChem** : This should point to the directory which contains the license files and also the basis subdirectory with basis set and effective core potential data. Throughout this document, this directory is called "the TeraChem directory."
* **LD\_LIBRARY\_PATH** : This is a system variable, which points to the directories containing dynamic libraries. The $TeraChem/lib directory should be included at the beginning of this list.
* **CUDA\_VISIBLE\_DEVICES** : This is a system variable which is used by the CUDA driver. If this variable is set, only GPUs listed will be visible to programs using CUDA. Setting this is the recommended way to control the usage of GPUs by TeraChem. Although it is also possible to control GPU usage in the input file or through the command line, setting this environment variable is the most effective way accomplish this goal. Note that the GPUs are reordered when this environment variable is used. For example,

```
export CUDA_VISIBLE_DEVICES=0,2
```

* **MagmaMinN** : Matrices of size NxN and larger will be diagonalized using MAGMA routines (where N is the value of the environment variable).
* **MagmaNGPUs** : When MAGMA is used, it will exploit N GPUs (where N is the value of the environment variable). These GPUs will be the first N which TeraChem sees. Please note that these are NOT necessarily the same as the GPUs which TeraChem is using for the electronic structure. As discussed below, you can control the GPUs which TeraChem uses either in the input file or through the command line. However, MAGMA will not respect that list. So, for example, if you run TeraChem as

```
terachem --gpus=23 start.in
```

then TeraChem will use the third and fourth GPU as the first and second GPU in the calculation. However, MAGMA will use the first GPU in the system (GPU #0). This can be very confusing and the easiest way to avoid problems is to restrict the visible GPUs to the ones desired by using the CUDA\_VISIBLE\_DEVICES environment variable. To accomplish the effect that the user probably desired above (that the TeraChem job uses only the third and fourth GPU), one would then type:

```
export CUDA_VISIBLE_DEVICES=2,3
terachem --gpus=01 start.in
```

This will restrict the visible GPUs to the third and fourth, which are then addressed as 0 and 1 when TeraChem runs. If you were then to set MagmaNGPUs to 3, the program would terminate with an error (because only 2 GPUs are visible).
