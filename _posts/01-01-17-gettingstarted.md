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

```Matlab
%Replace next line with your appropiate path to Mi-Sim directory'
misim_user_path = 'mysoftware/misim';
g=genpath(misim_user_path);
addpath(g);
```

## <a name="qs"></a>Quick Start

To start the GUI use:

```Matlab
MI_SIM
```

from the <span style="font-family:Courier;">MATLAB</span> command-line.

## <a name="usg"></a>User-Guide

You can download the user-guide via the link below. This document contains complete examples to start using the
<span style="font-family:Courier;">MI-Sim</span> GUI.
        


