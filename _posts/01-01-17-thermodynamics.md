---
layout: page
title:  Thermodynamics module
date:   01-01-17 00:00:00
category: doc
order: 2
---
## Contents

* [Screenshot](#Screenshot)
* [Description](#Description)
* [Reference](#Reference)

## <a name="Screenshot"></a>Screenshot

![alt text](https://raw.githubusercontent.com/MI-SIM/MI-SIM.github.io/master/_posts/thermo.png "Thermodynamic Inhibition Calculator Screenshot")

## Description

This module is available upon selection of the *thermodynamics* growth model from the <span style="font-family:Courier;">MI-Sim</span>
interface. At present, the thermodynamics is modelled only for the inhibition function, $I_2$, applicable to the cooperation/syntrophy and
three-species motifs. The growth model functions, $f_n$, default to Monod form in all cases. Furthermore, thermodynamic inhibition only has meaning 
in microbial systems and should not be used for interactions at higher trophic scales.

The thermodynamic calculator comprises three steps:

* **System specification**: The user should enter the operating temperature (K), reaction $\Delta G^0$ (kJ/mol), and the
number of reactants ($r$) and products ($p$) in the reaction. $\Delta G^0$ can be set to zero if the user wishes to automatically calculate the
$\Delta G$ value for each component of the reaction, or enter the cumulative value for all known compounds and calculate the remainder using the
calculator. Although $r$ and $p$ are set to one in all motif reactions, it is necessary here to specify the actual reaction stoichiometry to 
properly define its thermodynamics. Hence, there may be more reactants or products involved that are not explicitly modelled by 
<span style="font-family:Courier;">MI-Sim</span>. A simple text display of the reaction is provided to indicate the substrates, $S_n'$ and biomass 
$X_n$ involved in the conversion.

* **Compound specification**: In the central block of the calculator, the user may input stoichiometric information for each reactant and product
featured in the reaction. This includes the number of moles of substrate product, the molar mass of each compound (g/mol) and, if required, the option
to calculate the Gibbs Free Energy for each compound. For the latter, the user must specify the compound using drop-down menus to choose the chemical 
system where it is found, and its state (e.g., solid, liquid, aqueous, gas). For product substrates, the user must specify the stoichiometric
coefficient, $\gamma_n$, for each additional compound in the reaction.

* **Calculation**: The calculation of the thermodynamic inhibition function is executed by pressing the *Calculate* button. The functions
described [here](http://mi-sim.github.io//doc/misiminterface.html#thermo) are computed using the values provided by the user:

$$I_2 = f(T,\Delta G,S_\nu,S_\pi)$$

    where $S_\nu$ are the substrate reactants and $S_\pi$ the substrate products, and $S_n'=(S_\nu,S_\pi)$. The values for the compound specific $\Delta G_n^0$ at temperature $T$
are taken from the $\Delta G^0$ tables at saturation pressure provided in Amend and Shock (2001). Polynomial curve fitting of order 2 is used to
determine the $\Delta G^0$ values for the user-specified temperature, based on the temperature dependent curves developed from the values in these 
tables.

    The *Add Sn to ODE* function automatically defines equations for the additional substrates ($S_{\nu,new}$ and $S_{\pi,new}$) not included in the selected motif.
In the case additional reactants are included, a reconfiguration of the growth function for biomass X_n is required to account for its growth on this
additional substrate. The generic form of the additional equations are as follows:

$$\frac{dS_{\nu,new}}{dt}=-DS_{\nu,new}-f_{new}X_nI_2$$

$$\frac{dX_n}{dt}=-DX_n+Y_{new}f_{new}X_nI_2-k_{dec,n}X_n$$

$$\frac{dS_{\pi,new}}{dt}=-DS_{\pi,new}+\gamma_{new}(1-Y_n)f_nX_nI_2$$     
 
### Reference

Amend, J.P. and  Shock, E.L. (2001). Energetics of overall metabolic reactions of thermophilic and hyperthermophilic Archaea and bacteria. 
*FEMS Microbiol Rev.*, **25**(2), 175-243.
 
