---
layout: page
title:  GUI Interface
date:   01-01-17 00:00:00
category: doc
order: 1
---
## Contents

* [Screenshot](#Screenshot)
* [Description](#Description)
* [Menus](#Menus)
* [Models](#Models)
* [Plots](#Plots)
* [Simulation](#Simulation)
* [Reporting](#Reporting)
* [Options](#Options)

## <a name="Screenshot"></a>Screenshot

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/screenshot.png "MI-Sim Screenshot")

## <a name="Description"></a>Description

Mathematical modelling of ecological interactions is affected by the model objective (e.g., observation, prediction, 
control), the knowledge available to inform the model and the structural complexity necessary to adequately describe
the system or motif and numerous analysis methods exist, accordingly. The software we present here focuses strictly 
on a mechanistic understand- ing of ecological interactions and, more specifically, the analysis of microbial networks
for two or three species and associated substrates. However, the software is generic and the tools are not specific to
microbial ecology. We also consider a mechanistic approach to model development, in which systems of Ordinary Differential 
Equations (ODEs) are used to describe the dynamics of and interactions between the individual biotic and abiotic components.

The <span style="font-family:Courier;">MI-Sim</span> software provides a user-friendly environment in which ecologists, biologists and mathematicians can
rapidly characterise the dynamics of two or three species ecological motifs robustly, without the necessity to
develop their own code or understand the mathematical details of dynamical systems analysis.

## <a name="Menus"></a>Menus

### <a name="Models"></a>Models

In this version of <span style="font-family:Courier;">MI-Sim</span>, six common ecological motifs describing interactions between two distinct species,
plus one extended motif that consists of three interacting species are modelled. The seven motifs
are simple networks commonly observed at both micro- and macro-scales, and provide a theoretical basis by which
biologists and ecologists can understand and visualise ecological interactions.

The motifs included in <span style="font-family:Courier;">MI-Sim</span> are expressed as a series of ODEs, which describe the microbial growth,
catabolic conversion processes, and species interactions within the system. The equations are developed using 
a standard mass-balance approach coupled with stoichiometric information
describing the chemical transformation between reactants and products in the system.

The models currently available in <span style="font-family:Courier;">MI-Sim</span> are described as follows:


#### Food Chain
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/fc.png "Food Chain Motif") 

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1 - f_2X_2$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$

#### Substrate Competition
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/sc.png "Substrate Competition Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1 - f_2X_2$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$


#### FC (Food Chain) with Product Inhibition
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/fcpi.png "FC with Product Inhibition Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1I_3$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1I_3 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1I_3 - f_2X_2$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$

$\frac{dS_3}{dt} = -DS_3 + f_2X_2$

$I_3 = \frac{1}{1+\frac{S_3}{K_{i,3}}}$


#### No Common Metabolites
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/ni.png "No Interaction Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = D(S_{2,in} - S_2) - f_2X_2$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$


#### Syntrophy
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/syn.png "Syntrophy Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1I_2$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1I_2 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1I_2 - f_2X_2$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$

$I_2 = \frac{1}{1+\frac{S_2}{K_{i,2}}}$


#### Waste Product Inhibtion
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/wpi.png "Waste Product Inhibition Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1$

$\frac{dX_2}{dt} = -DX_2 + Y_3f_3X_2I_2 - k_{dec,3}X_2$

$\frac{dS_3}{dt} = D(S_{3,in}-S_3) - f_3X_2I_2$

$I_2 = \frac{1}{1+\frac{S_2}{K_{i,2}}}$


#### Three species (Food-web)
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/ths.png "Food Web Motif")

ODE model:

$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$

$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$

$\frac{dS_2}{dt} = D(S_{2,in} - S_2) + \gamma_0(1-Y_1)f_1X_1 - f_2X_2I_2$

$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2I_2 - k_{dec,2}X_2$

$\frac{dS_3}{dt} = D(S_{3,in}-S_3) + \gamma_1(1-Y_2)f_2X_2I_2 - f_3X_3 - \gamma_2f_1X_1$

$\frac{dX_3}{dt} = -DX_3 + Y_3f_3X_3 - k_{dec,3}X_3$

$I_2 = \frac{1}{1+\frac{S_3}{K_{i,2}}}$


#### Growth functions

The growth functions defined, generically, as $f_p$ in the ODE models may take any form. At present, <span style="font-family:Courier;">MI-Sim</span> only includes 
the option to use the Monod growth function:

$f_{p} = \frac{k_{m,p}S_n}{K_{S,p}+S_n}$

However, future versions of the software will include options to use other common functions, such as Contois, Tessier, Moser, Andrews, Logistic,
and the inclusion of thermodynamic representation for growth and inhibition.


#### Description of symbols

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/symbols.png "Description of symbols")

### <a name="Plots"></a>Plots

#### Solutions

#### Trajectories

### <a name="Simulation"></a>Simulation

#### Single-Point

#### Multiple-Point

#### Basin of Attraction

#### Phase Portrait

### <a name="Reporting"></a>Reporting

### <a name="Options"></a>Options
