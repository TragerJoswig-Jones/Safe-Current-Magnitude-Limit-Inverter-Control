# Safe-Current-Magnitude-Limit-Inverter-Control
This repository contains source code necessary to reproduce the results presented in the following paper:
[Safe Control of Grid-Interfacing Inverters with Current Magnitude Limits](https://arxiv.org/abs/2409.13890)  

Authors: Trager Joswig-Jones and Baosen Zhang  

University of Washington 


# Motivation
Grid-interfacing inverters allow renewable resources to be connected to the electric grid and offer fast and programmable control responses. However, inverters are subject to significant physical constraints. One such constraint is a current magnitude limit required to protect semiconductor devices. While many current limiting methods are available, they can often unpredictably alter the behavior of the inverter control during overcurrent events leading to instability or poor performance.

In this paper, we present a safety filter approach to limit the current magnitude of inverters controlled as voltage sources. The safety filter problem is formulated with a control barrier function constraint that encodes the current magnitude limit. To ensure feasibility of the problem, we prove the existence of a safe linear controller for a specified reference. This approach allows for the desired voltage source behavior to be minimally altered while safely limiting the current output.

# Language and Dependencies
This respository contains code implemented in Python and can be run using Jupyter notebook or Google Colab. 


## Acknowledgments

The development of this code was supported in part by NSF grant ECCS-202353 and the State of Washington through the University of Washington Clean Energy Institute Graduate Student Fellowship.

The primary developer is Trager Joswig-Jones (@TragerJoswig-Jones).

This source code is available in the hope that it will be useful, but without any warranty and in no event shall the authors or copyright holders be liable for any claim, damages or other liability.

## Notes

The simulation results in this paper take the voltage magnitude to be 120 V. This should be the nominal voltage value not the voltage magnitude. Correcting this simply scales the simulation results. This is corrected in the code in this repository now.

The control Lyapunov function used in the paper is $V(x) = (x - x^{\*})^\top (x - x^{\*})$. The paper incorrectly states that $V(x) = x^\top x$. 

# Citing

If you find this repository useful in your work, we kindly request that you cite the following [publication](https://scholarspace.manoa.hawaii.edu/items/591fb26c-8ba6-44e3-85b8-e96d02abe496):
```
@inproceedings{Joswig-Jones_Zhang_2025,
      title={Safe Control of Grid-Interfacing Inverters with Current Magnitude Limits},
      url={http://dx.doi.org/10.24251/HICSS.2025.363},
      DOI={10.24251/hicss.2025.363},
      booktitle={2025 Hawaii International Conference on System Sciences},
      publisher={Hawaii International Conference on System Sciences},
      author={Joswig-Jones, Trager and Zhang, Baosen},
      year={2025}
}
```
