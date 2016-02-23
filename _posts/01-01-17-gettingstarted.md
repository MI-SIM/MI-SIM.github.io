---
layout: page
title:  Getting Started
date:   01-01-17 00:00:00
category: inst
order: 1
---

## Contents

* [Download](#Download)
* [Installation](#Installation)
* [Quick Start](#qs)
* [User-Guide](#usg)

## <a name="Download"></a>Download

* [MI-Sim Ver. 1.0](http://www.mathworks.com/matlabcentral/fileexchange/55492-mi-sim) **- February 2016**
 
## <a name="Installation"></a>Installation

To install <span style="font-family:Courier;">MI-Sim</span>, copy the downloaded zip file to an appropriate directory 
(e.g., a <span style="font-family:Courier;">MATLAB</span> working directory) and unzip it.
Next, you will need to add <span style="font-family:Courier;">MI-Sim</span> to the <span style="font-family:Courier;">MATLAB</span> path:

It is recommended you add the directory to the permanent <span style="font-family:Courier;">MATLAB </span> path using the instructions found at:
[<span style="font-family:Courier;">MATLAB</span> search path](http://uk.mathworks.com/help/matlab/matlab_env/add-remove-or-reorder-folders-on-the-search-path.html).

Alternatively, you can add the <span style="font-family:Courier;">MI-Sim</span> directory and sub-directories to the \matlab path.
You will need to execute the following lines of code every time you initiate a new <span style="font-family:Courier;">MATLAB</span> session.

<pre class="prettyprint lang-matlab">
    <code>
<span class="comment">%Replace next line with an appropriate path to your Mi-Sim directory</span>
misim_user_path = <span class="string">'mysoftware/misim'</span>;
g=genpath(misim_user_path);
addpath(g);
    </code>
</pre>

## <a name="qs"></a>Quick Start

To start the GUI with default motif ('Syntrophy') and growth function ('Monod') use:

<pre class="prettyprint lang-matlab">
    <code>
MI_SIM
    </code>
</pre>

from the <span style="font-family:Courier;">MATLAB</span> command-line.

Alternatively, specifying the motif and growth function names as input arguments will set-up the GUI environment accordingly.

|Ecological interaction |Motif name                | shortname |
|-----------------------|:------------------------:|-----------|
|Commensalism           |Food chain                |'comm'     |
|Competition            |Substrate competition     |'comp'     |
|Predation              |FC with product inhibition|'pred'     |
|No interaction         |No common metabolites     |'no_i'     |
|Cooperation            |Syntrophy                 |'coop'     |
|Amensalism             |Waste product inhibition  |'amen'     |
|Competition/Syntrophy  |Three species food-web    |'thre'     |


||Growth function|| shortname||Availability||
||---------------||:--------:||------------||
||Monod          ||'mon'     ||$\checkmark$||
||Contois        ||'con'     ||N/A         ||
||Tessier        ||'tes'     ||N/A         ||
||Moser          ||'mos'     ||N/A         ||
||Logistic       ||'log'     ||N/A         ||
||Andrews        ||'and'     ||N/A         ||
||Thermodynamic  ||'the'     ||N/A         ||

For example, to start the GUI with a syntrophic motif and the Monod growth function:

<pre class="prettyprint lang-matlab">
    <code>
MI_SIM('coop','mon')
    </code>
</pre>

## <a name="usg"></a>User-Guide

You can download the user-guide via the link below [COMING SOON]. This document contains complete examples to start using the
<span style="font-family:Courier;">MI-Sim</span> GUI.
        


