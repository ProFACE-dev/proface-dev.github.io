---
layout: default
---
# Development

## Development timeline @ Politecnico di Milano \[PoliMi\]
![](images/timeline.png)

------------------------------------------------------------------------
## History

After an initial concept in 2017, the software was developed in 2018 as a Matlab® tool to post process Finite Element analyses, then its concept was patented and its results published.

![](images/MC.png)
*Failure probability calculation by MC simulations: a) schematics of the plate with a hole; b) example of defects sampled in one simulation; critical defects obtained by 100 simulations with c) low applied stress and high defect density or d) high applied stress and low defect density. \[1\]*

Software predictions were successfully compared to a series of Montecarlo simulations on notched specimens.

![](images/notched_spec.png)
*Geometry of the notched specimens. \[1\]*

![](images/dfx_distribution.png)
*Example of defect distribution in the samples: a) size and position of the defects detected; b) analytical description of CT measurements. \[1\]*

The notched specimens were first analysed with X-ray computed tomography and then fatigue tested. The experimental failure loads were also predicted by detailed crack growth analyses with NASGRO® and compared with ProFACE results.

![](images/NASGRO.png)
*Input for the NASGRO simulations: a) example position and life expected by ProFACE for the ten most critical defects detected in one of the samples; b) maximum principal stress acting on the plane containing the critical defect (in this example, z=0). Fatigue life estimation by ProFACE and NASGRO simulations: c) cdf for the batch; d) estimate for every sample. \[1\]*

### From model to software

The initial version of the software was then tested in cooperation with Airbus. The software was later developed as a stand-alone compiled version and delivered to the European Space Agency (ESA).

### From alfa version to ProFACE 1.0

The initial concept was extended, following the results of fatigue tests on benchmark components (“wishbones”) that were manufactured by MTC and tested by ESA \[2\].

![](images/WB_build.png)
*a) Image of build layout and b) photograph of one of the four identical manufactured builds. \[2\]*

The analysis of results of machined and as-built components clarified that a fracture-based fatigue assessment, as the one implemented in ProFACE, is the only one able to provide good life predictions, provided that residual stresses were taken into account \[2\].

![](images/WB_fractographies.png)
*Defects detected on the fracture surfaces of machined (M) and as-built (AB) benchmark components. \[2\]*

------------------------------------------------------------------------
### Version 2.0

ProFACE was further developed in the version 2.0, which allows the user to:

- describe material behaviour of different stress ratios through user input of the Haigh diagram and fatigue thresholds described by NASGRO equation;
- consider volumetric defects that can randomly occur in any position in the material volume, and surface features related to net-shape surfaces;
- residual stresses on the external layers, characterized by the surface value and the local gradient, to fully represent the *local stress* state.

The results obtained by ProFACE 2.0 \[3\] allowed to obtain very good life predictions for cylindrical specimens and “wishbones”.

![](images/SN_HCF.png)
*Failure probability estimated by ProFACE for the cylindrical specimens: (a) machined fatigue specimens and (b) as-built fatigue specimens. \[3\]*

![](images/WB_FEM.png)
*Scheme of the numerical simulations of the wishbones: (a) frontal view of the load and boundary conditions; (b) back view of the load and boundary conditions and \(c\) zones of the application of different residual stress field. \[3\]*

![](images/FN_WB_2_0.png)
*ProFACE analysis of wishbone specimens: (a) machined wishbones and (b) as-built wishbones. \[3\]*

------------------------------------------------------------------------
### Version 2.1

The current version 2.1 introduces an additional type of material strength model. The new model allows to simulate fatigue behaviour in presence of defects by means of the NASGRO equation for crack propagation.

This new implementation further improved the fatigue life predictions on the benchmark “wishbones”, with a reduced scatter in the finite life region.
![](images/FN_WB_AB_2_1.png)
*ProFACE 2.1 analysis of as-built wishbone specimens with the new material strength model.*

------------------------------------------------------------------------
## Future developments

After the successful benchmark on components manufactured by PBF-LB in AlSi10Mg, another ongoing research project with The MTC as partner is devoted to testing components manufactured in Ti6Al4V.

This activity will allow to:

- establish a database of crack growth properties for annealed Ti6Al4V merging new data with PoliMi database;
- evaluate the effect of chemical milling;
- check the ProFACE predictions at different stress ratios.

Other developments of the software tool are planned in:

- SmartPROFACE project (a consortium led by PoliMI with partipants: The MTC, BEAMIT, Thales France, Leonardo) where the outputs of defect acceptability maps will be adopted for the qualification of space components printed in Ti6Al4V and Scalmalloy®;
- EU project NEUMANN, where ProFACE will be adopted for the assessment of aeroengine components in close cooperation with GE Avio (Rivalta, Italy).
  
------------------------------------------------------------------------
## References

\[1\] Romano S., Miccoli S., and Beretta S. (2019). “A new FE post-processor for probabilistic fatigue assessment in the presence of defects and its application to AM parts” *International Journal of Fatigue* 125, 324-341

\[2\] Beretta S., Patriarca L., Gargourimotlagh M., Hardaker A., Brackett D., Salimian  M., Gumpinger J., and Ghidini. T. (2022) “A benchmark activity on the fatigue life assessment of AlSi10Mg components manufactured by L-PBF” *Materials & Design* 218, 110713

\[3\] Sausto F., Romano S., Patriarca L., Miccoli S., and Beretta S. (2022) “Benchmark of a probabilistic fatigue software based on machined and as-built components manufactured in AlSi10Mg by L-PBF” *International Journal of Fatigue* 165, 107171
