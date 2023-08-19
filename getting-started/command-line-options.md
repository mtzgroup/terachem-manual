# Command Line Options

Most often, the TeraChem program is run with a single command line option – the name of the input file containing directives. For example,

```shell
terachem start.sp
```

However, there are some other command line options that may be useful. These may be listed by running

```shell
terachem -h
```

{% code fullWidth="true" %}
```
TeraChem Usage: 
    /home/toddmtz/GitControlled/terachem/build/bin/terachem [options] startfile
Options: 
    -h|--help               Show usage information 
    -v|--version            Print version information 
    -u|--update             Download the latest TeraChem release 
    -f|--functionals        Print available DFT functionals 
    -gxyz|--gpus=xyz        Use GPUs xyz (0-9/a-f). This command may be repeated to use multiple GPUs. 
    -Ux|--UseMPI=x          Use MPI named ports for input. x=2 FMS interface. 
    -Mxxx|--MPIPort=xxx     Use xxx as MPI named port (default=terachem_port) 
    -T|--ThcMPI             Use MPI for THC-CC calculations 
    -E|--ExMod              Use MPI for exciton model 
    -s|--server             Start TeraChem as a Protocol Buffer server 
    -ifile|--inputfile=file Input file for TeraChem
```
{% endcode %}



* The MPI named ports are not for MPI-based parallelization. TeraChem currently only runs on a single node (using up to 16 GPUs). Instead, the commands --UseMPI and --MPIPort are for an advanced feature of TeraChem which allows TeraChem to run as a server, waiting for MPI socket communication to carry out calculations. This feature is being tested for coupling between TeraChem and Amber/FMS.
* The Amber/FMS interfaces are not currently documented or available for general use.

The point engine mode is intended for use with a separately distributed Python module. It is possible to use the same interface for a general program which is described in section 7, but the protocol is subject to change. TeraChem will also print out specifications of expected communications when running in this mode. Only one program can be connected with each server.

* Note that the following are equivalent:

```
terachem start.sp
```

and

```
terachem --inputfile=start.sp
```

* To use the second and fourth GPUs:

```
terachem --gpus=13
```

Note that the numbering starts from 0. Also, please note that the GPUs are numbered as TeraChem finds them. GPUs which are not visible to TeraChem will not be counted in the list. Note that the use of --gpus or -g will override any gpus line in the input file.

* It is possible to hide GPUs from TeraChem and all other GPU programs using the CUDA\_VISIBLE\_DEVICES environment variable. For example, to ensure that only the second and third GPUs are visible, use:&#x20;

```
export CUDA_VISIBLE_DEVICES="1,2"
```

Note that the numbering starts from zero.

* To get a list of all the GPUs, use the nvidia-smi program supplied with CUDA by NVIDIA:

```
nvidia-smi
```
