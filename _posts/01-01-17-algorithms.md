---
layout: page
title:  Algorithms
date:   01-01-17 00:00:00
category: doc
order: 2
---

## Contents
* [Algorithm 1: Single Point Analysis](#spa)
* [Algorithm 2: Multiple Point Analysis](#mpa)
* [Algorithm 3: Basin of Attraction](#boa)
* [Algorithm 4: Phase Portrait](#phase)

## <a name="spa"></a>Single Point Analysis
The system of ODEs, $F(\tilde{x}(t))$ are solved algebraically to find the fixed-point solutions, $\tilde{x}^{g,*}$, where $g$
represents the number of fixed-points found. $\tilde{x}$ is the vector of variables ($X$ and $S$) associated with the motifs.
Two methods are available for analysis of the stability of the fixed-points *Linear Stability Analysis* and the *Routh-Hurwitz* criterion. 
In the former, $\epsilon$ defines the tolerance threshold for stability.

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/spa.png "Single Point Analysis Algorithm")

## <a name="mpa"></a>Multiple Point Analysis
This is an extension of the [Single Point Analysis](#spa), extended for multiple points ($s_i$) within the range ($a_i$,$b_i$) for a pair of 
parameters ($\theta_{i}$), where $i = (1,2)$.  In biological terms, the chosen parameters may represent operational properties of the system 
(e.g., dilution rate $D$, substrate input concentration $S_{in}$) or of the organisms themselves (e.g., growth rates, substrate yields),
and thus can be used to test the effect of these parameters on the behaviour of the system itself.

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/mpa.png "Multiple Point Analysis Algorithm")

## <a name="boa"></a>Basin of Attraction
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/boa.png "Basin of Attraction Algorithm")

## <a name="phase"></a>Phase Portrait
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/pp.png "Phase Portrait Algorithm")
