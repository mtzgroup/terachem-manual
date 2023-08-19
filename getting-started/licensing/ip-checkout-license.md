# IP Checkout License

Starting with TeraChem v1.9, it is also possible to use a checkout type of license. This requires that your compute nodes have access to the open internet. If compute nodes do not have internet access, it is possible to forward the license traffic through a local HTTP proxy (for instance, running on a head node in a cluster) that has internet access and is accessible to the compute nodes. See section [http-forwarding.md](http-forwarding.md "mention") for more details on HTTP forwarding. The basic idea of checkout type licenses is that the compute node will contact a PetaChem license server (directly or through an HTTP proxy), which will then check that a valid license exists. In this way, the identity of the node running a job is not restricted and the restriction is instead on the number of nodes that can simultaneously run jobs. To use this licensing mode, you must first contact help@petachem.com and they will determine the number of simultaneous nodes that you qualify for. They will also provide you with a license file which contains your unique token. This should be protected, since anyone with knowledge of this token could run TeraChem instances under your license (which would use up your available slots).

This license file should be saved as **license.key** in the TeraChem directory. For reference, here is an example **license.key** file (the license key is not valid - this is for demonstration purposes only):

{% code title="license.dat" %}
```
key Ki56jjjKKKK
server 54.208.252.40:8877
```
{% endcode %}
