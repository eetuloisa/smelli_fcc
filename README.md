# Smelli with FCC-ee Higgs and electroweak precision observables  

This package extends smelli v2.4.2 by introducing the projected FCC-ee sensitivities for a number of Higgs and electroweak precision observables (see also the related [flavio_fcc repository](https://github.com/eetuloisa/flavio_fcc)).
Whilst we eventually hope to incorporate the features as part of the main program, currently the best way to access the FCC-ee sensitivity estimates is to 
1. Create a virtual environment with a functioning flavio v2.6.1 and smelli v2.4.2 default installations.
2. Make a copy of the 'smelli' directory found in this repository and replace the default smelli installation with the FCC-ee version found here. Do the same with the FCC-ee version of flavio, replacing the default version.
4. The package can now be used in the same way as the unmodified smelli package. 

For the full set of observables added, see the appendices in arXiv:2501.xxxxx. 
If new to smelli, please consult the main [smelli page](https://github.com/smelli/smelli) and the references therein.

The observables are contained in two data sets: likelihood_ewpt_fccee.yaml and likelihood_higgs_fccee.yaml. 
These can be included in the instantiation of the global likelihood object in smelli, for instance:
```
gl = smelli.GlobalLikelihood(include_likelihoods=
        {
        'likelihood_ewpt_fccee.yaml',
        'likelihood_higgs_fccee.yaml',
        'fast_likelihood_quarks.yaml'
         })
```
