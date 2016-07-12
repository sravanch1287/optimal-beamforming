Optimal Multiuser Transmit Beamforming: A Difficult Problem with a Simple Solution Structure
==================

This is a code package is related to the following “lecture note” article:

Emil Björnson, Mats Bengtsson, and Björn Ottersten, “[Optimal Multiuser Transmit Beamforming: A Difficult Problem with a Simple Solution Structure](http://arxiv.org/pdf/1404.0408),” IEEE Signal Processing Magazine, vol. 31, no. 4, pp. 142-148, July 2014.

The package contains a simulation environment, based on Matlab, that reproduces all the numerical results and figures in the article. *We encourage you to also perform reproducible research!*


##Abstract of Article

Transmit beamforming is a versatile technique for signal transmission from an array of N antennas
to one or multiple users [1]. In wireless communications, the goal is to increase the signal power at
the intended user and reduce interference to non-intended users. A high signal power is achieved by
transmitting the same data signal from all antennas, but with different amplitudes and phases, such
that the signal components add coherently at the user. Low interference is accomplished by making the
signal components add destructively at non-intended users. This corresponds mathematically to designing
beamforming vectors (that describe the amplitudes and phases) to have large inner products with the
vectors describing the intended channels and small inner products with non-intended user channels.

If there is line-of-sight (LoS) between the transmitter and receiver, beamforming can be seen as forming
a signal beam towards the receiver; see Figure 1. Beamforming can also be applied in non-LoS scenarios,
if the multipath channel is known, by making the multipath components add coherently or destructively.

Since transmit beamforming focuses the signal energy at certain places, less energy arrives to other
places. This allows for so-called space-division multiple access (SDMA), where K spatially separated
users are served simultaneously. One beamforming vector is assigned to each user and can be matched
to its channel. Unfortunately, the finite number of transmit antennas only provides a limited amount of
spatial directivity, which means that there are energy leakages between the users which act as interference.

While it is fairly easy to design a beamforming vector that maximizes the signal power at the intended
user, it is difficult to strike a perfect balance between maximizing the signal power and minimizing
the interference leakage. In fact, the optimization of multi-user transmit beamforming is generally a
nondeterministic polynomial-time (NP) hard problem [2]. Nevertheless, this lecture shows that the optimal
transmit beamforming has a simple structure with very intuitive properties and interpretations. This
structure provides a theoretical foundation for practical low-complexity beamforming schemes.


##Content of Code Package

The paper contains 2 simulation figures, Figure 3(a) and Figure 3(b). These are generated by the Matlab script simulationFigure3.m. 

The package contains 7 additional Matlab functions: functionBRBalgorithm_cvx.m, functionFairnessProfile_cvx.m, functionFeasibilityProblem_cvx.m, functionHeuristicPowerAllocation.m, functionMRT.m, functionSLNRMAX.m, functionZFBF.m. These are called by the main script and originates from the Matlab code distributed with the following book:

Emil Björnson, Eduard Jorswieck, “[Optimal Resource Allocation in Coordinated Multi-Cell Systems,” Foundations and Trends in Communications and Information Theory](http://kth.diva-portal.org/smash/get/diva2:608533/FULLTEXT01), vol. 9, no. 2-3, pp. 113-381, 2013.

The optimal beamforming is computed as a sequence of convex optimization problems, which are implemented and solved using the modeling language [CVX](http://cvxr.com/cvx/).

See each file for further documentation. 


##Acknowledgements

This work was supported by the International Postdoc Grant 2012-228 from the Swedish Research Council and by the
European Research Council under the European Community’s Seventh Framework Programme (FP7/20072013)/ERC Grant
228044.


##License and Referencing

This code package is licensed under the GPLv2 license. If you in any way use this code for research that results in publications, please cite our original article listed above.
