---
layout: page
title:  GUI Interface
date:   01-01-17 00:00:00
category: inst
order: 2
---

## Screenshot

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/screenshot.png "MI-Sim Screenshot")

## Menus

### Models

#### Food Chain
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/fc.png "Food Chain Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1 - f_2X_2$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$\\

#### Substrate Competition
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/sc.png "Substrate Competition Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1 - f_2X_2$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$\\

#### FC (Food Chain) with Product Inhibition
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/wpi.png "FC with Product Inhibition Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1I_3$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1I_3 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1I_3 - f_2X_2$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$\\
$\frac{dS_3}{dt} = -DS_3 + f_2X_2$\\
$I_3 = \frac{1}{1+\frac{S_3}{K_{i,3}}}$\\

#### No Common Metabolites
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/ni.png "No Interaction Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = D(S_{2,in} - S_2) - f_2X_2$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$\\

#### Syntrophy
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/syn.png "Syntrophy Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1I_2$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1I_2 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1I_2 - f_2X_2$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2 - k_{dec,2}X_2$\\
$I_2 = \frac{1}{1+\frac{S_2}{K_{i,2}}}$\\

#### Waste Product Inhibtion
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/fcpi.png "Waste Product Inhibition Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = -DS_2 + \gamma(1-Y_1)f_1X_1$\\
$\frac{dX_2}{dt} = -DX_2 + Y_3f_3X_2I_2 - k_{dec,3}X_2$\\
$\frac{dS_3}{dt} = D(S_{3,in}-S_3) - f_3X_2I_2$\\
$I_2 = \frac{1}{1+\frac{S_2}{K_{i,2}}}$\\

#### Three species (Food-web)
![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/ths.png "Food Web Motif")
ODE model:\\
$\frac{dS_1}{dt} = D(S_{1,in} - S_1) - f_1X_1$\\
$\frac{dX_1}{dt} = -DX_1 + Y_1f_1X_1 - k_{dec,1}X_1$\\
$\frac{dS_2}{dt} = D(S_{2,in} - S_2) + \gamma_0(1-Y_1)f_1X_1 - f_2X_2I_2$\\
$\frac{dX_2}{dt} = -DX_2 + Y_2f_2X_2I_2 - k_{dec,2}X_2$\\
$\frac{dS_3}{dt} = D(S_{3,in}-S_3) + \gamma_1(1-Y_2)f_2X_2I_2 - f_3X_3 - \gamma_2f_1X_1$\\
$\frac{dX_3}{dt} = -DX_3 + Y_3f_3X_3 - k_{dec,3}X_3$\\
$I_2 = \frac{1}{1+\frac{S_3}{K_{i,2}}}$\\

### Plots

#### Solutions

#### Trajectories

### Simulation

#### Single-Point

#### Multiple-Point

#### Basin of Attraction

#### Phase Portrait

### Reporting

### Options
