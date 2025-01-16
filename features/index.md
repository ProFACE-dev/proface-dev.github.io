---
layout: default
---

# Features

The basic concept of the ProFACE software, aimed at describing the reliability of components with defects, is to correctly consider the size effect, that is the theoretical prediction (confirmed by experiments \[1\]), that the distribution of largest defect increases with the material volume.

This effect can be modelled (for a given material volume) by:

- weakest link analysis;
- statistics of extremes.

ProFACE adoptes the second approach, that is more robust and simple than the dirtiness curves needed by the weakest link approach.


![](images/size_fx.png)
*Evidence of the size effect for defects at the origin of fatigue failures in specimens manufactured by PBF-LB: a) specimens tested; b) probability paper of defects. \[1\]*

------------------------------------------------------------------------
The key point of ProFACE 2.0 for the probabilistic analysis is a patented component discretization in different parts:

- surface elements, affected by surface features of net-shape AM surfaces;
- a surface volume where the volumetric defects can randomly be located close to the surface;
- internal volume where volumetric defects can randomly occur.

This discretizations allows the software to correctly calculate the failure probability of a component, where the volumetric defects can randomly occur close to the surface or within the component volume.

![](images/regions.png)
*Schematic of the analysis performed by ProFACE: (a) distinction between volumetric and superficial analysis and (b) weakest link applied to both volumes and surfaces. \[2\]*


------------------------------------------------------------------------
## Ingredients

The first **mechanical ingredient** of ProFACE 2.0 is a suitable description of fatigue in presence of defects through:

- Kitagawa diagram (fatigue limit as a funtion of defect size) as a function of stress ratio defined by the user with the haigh diagram and the NASGRO equation for thresholds;
- a normalized S-N diagram defined by the user.

The two inputs allow the software to obtain a Kitagawa diagram for different number of cycles and stress ratios.

![](images/Normalized_SN.png)
*Schematic of the finite fatigue life model adopted in ProFACE for a general stress ratio R=-1: (a) normalized S–N curve and (b) generalized Kitagawa curves as a function of the number of cycles to failure. \[2\]*

The new approach implemented in ProFACE 2.1 permits the description of the relationship between limit stress and defect size for target life and stress ratios by interpolating **defect size-dependent S-N curves**.
![](images/ProFACE2_1.png)
*(a) S-N curves obtained from explicit fatigue crack growth calculations with NASGRO propagation equation. (b) Relationship between limit stress and defect size for a target life of 100 000 cycles, derived from the S-N curves.*

------------------------------------------------------------------------

The probabilistic ingredients are the two main parameters that determine the scatter of fatigue strength:

1.  a description of the inherent fatigue resistance by a scatter of the fatigue limit through a log-normal distribution (the scatter of fatigue strength is related also to life dispersion);

2.  the distribution of material anomalies divided in:

	– volumetric defects, obtained through a suitable ***extreme value statistics*** of data obtained with different experimental techniques (CT scan, anomalies at the origin of failures in witness specimens);

	– surface features, obtained by measuring the features at the origin of failures or accurately measuring the roughness of the net-shape surface (once again concepts of extreme value statistics have to be adopted for describing the size effect for the surface features).

![](images/surface.png)
  
------------------------------------------------------------------------
## References

\[1\] Romano S., Patriarca L., Foletti S., and Beretta S. (2018) “LCF behaviour and a comprehensive life prediction model for AlSi10Mg obtained by SLM.” *International Journal of fatigue* 117, 47-62

\[2\] Sausto F., Romano S., Patriarca L., Miccoli S., and Beretta S. (2022) “Benchmark of a probabilistic fatigue software based on machined and as-built components manufactured in AlSi10Mg by L-PBF” *International Journal of Fatigue* 165, 107171