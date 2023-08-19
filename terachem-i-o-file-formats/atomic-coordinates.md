# Atomic Coordinates

The coordinates file fed to the coordinates parameter should be either in XMol (also called "xyz") or PDB format. In an XMol coordinates file, the first line specifies the number of atoms, and the second line provides a description of the system (it can be left blank). Atomic coordinates are listed starting from the third line. All coordinates are either in Angstroms (default) or Bohrs (this can be specified in the start file). Here is an example coordinates file for a hydrogen molecule:

<pre data-title="h2.xyz"><code><strong>2
</strong><strong>Hydrogen Molecule -- Xmol format
</strong><strong>H 0.0 0.0 0.0
</strong><strong>H 0.7 0.0 0.0
</strong></code></pre>

Some jobs (for example, transition state search using NEB method) require several sets of coordinates (frames). In this case all frames should be listed in the coordinates file one by one, i.e.

{% code title="h2-2frames.xyz" %}
```
2
Hydrogen Molecule -- Xmol format frame 1
H 0.0 0.0 0.0
H 0.7 0.0 0.0
2
Hydrogen Molecule -- Xmol format frame 2
H 0.0 0.0 0.0
H 0.8 0.0 0.0
```
{% endcode %}

Note that there should be no blank lines between individual frames.

The PDB format often used for protein molecules is also supported and will be automatically assumed if the filename for the coordinates ends in ‘.pdb’. More details on PDB file format are available at&#x20;

```
http://www.wwpdb.org/docs.html
```
