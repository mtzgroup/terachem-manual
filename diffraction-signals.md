# Diffraction Signals

TeraChem can compute elastic and inelastic scattering signals for CAS-type (CASCI and CASSCF) wavefunctions, relevant for X-Ray and electron diffraction experiments.  &#x20;

Add some description of the basic theory here

Input parameters

<table><thead><tr><th width="226">Keyword</th><th width="93.33333333333331">Values</th><th>Description</th></tr></thead><tbody><tr><td>diffraction</td><td><strong>yes</strong>|no</td><td>yes triggers the computation of the diffraction signal</td></tr><tr><td>diff_lvalue</td><td><strong>-1</strong></td><td>Maximum l for rotational averaging</td></tr><tr><td>diff_s_start</td><td><strong>0.0</strong></td><td>Scattering vector range is diff_s_start...diff_s_end in increments of diff_delta_s (units of <span class="math">bohr^{-1}</span>)</td></tr><tr><td>diff_s_end</td><td><strong>10.0</strong></td><td></td></tr><tr><td>diff_delta_s</td><td><strong>0.1</strong></td><td></td></tr><tr><td>diff_axis_x</td><td><strong>0.0</strong></td><td>Axis for rotational averaging</td></tr><tr><td>diff_axis_y</td><td><strong>0.0</strong></td><td></td></tr><tr><td>diff_axis_z</td><td><strong>1.0</strong></td><td></td></tr><tr><td>diff_rotation_averaging</td><td><strong>0</strong>|1|2</td><td>0 = Uniform averaging of all molecular orientations<br>1 = <span class="math">cos^2(\theta)</span>distribution, parallel to specified axis<br>2 = <span class="math">sin^2(\theta)</span>distribution, perpendicular to specified axis</td></tr></tbody></table>
