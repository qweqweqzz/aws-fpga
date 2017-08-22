# AWS Vivado Flows

## Table of Content

1. [Overview](#overview)

2. [IP Integrator Project with Example Design](#ipiprojex)

3. [RTL Project with Example Design](#rtlprojex)

4. [RTL Project - New RTL Design](#rtlnew)



<a name="overview"></a>
# Overview  

This document covers top level steps (cheat sheet) for using a particular flow

For step by step instructions refer to the [Vivado Tutorials/Examples](./IPI_GUI_Examples.md) documentation.

At this time On-Premise flow is recommended with this environment.

Make sure the [HLx Setup Instructions](./IPI_GUI_Vivado_Setup.md) are followed and executed.

<a name="ipiprojex"></a>
# IP Integrator Project with Example Design

Create project directory

start vivado

## Execute example
See what examples are possible, type into TCL console.

aws::make\_ipi -examples

Type into TCL console based upon example needed.

aws::make\_ipi -examples <example requested>

## Implementing the Design/Tar file

In the Design Runs tab, right click on impl\_1 and select Launch Runs� . Click OK in the Launch Runs Dialog Box.  Click OK in the Missing Synthesis Results Dialog Box.

This will run both synthesis and implementation.

The completed .tar file is located in <project>.runs/faas\_1/build/checkpoints/to\_aws/<timestamp>.Developer\_CL.tar.  For information on how to create a AFI/GAFI with .tar from the design, following to the How To Create an Amazon FPGA Image (AFI) From One of The CL Examples: Step-by-Step Guide documentation.


## Opening Existing Vivado Project
Type into TCL console any time reopening the project.

When opening an existing Vivado project (IPI flow), the following TCL command must be run when the project first opens or an error could show up in simulation/implementation flow.

aws::make\_ipi

<a name="rtlprojex"></a>
# RTL Project with Example Design

Create project directory

start vivado

## Execute example
See what examples are possible, type into TCL console.

aws::make\_rtl -examples

Type into TCL console based upon example needed.

aws::make\_rtl -examples <example requested>

## Implementing the Design/Tar file

In the Design Runs tab, right click on impl\_1 and select Launch Runs� . Click OK in the Launch Runs Dialog Box.  Click OK in the Missing Synthesis Results Dialog Box.

This will run both synthesis and implementation.

The completed .tar file is located in <project>.runs/faas\_1/build/checkpoints/to\_aws/<timestamp>.Developer\_CL.tar.  For information on how to create a AFI/GAFI with .tar from the design, following to the How To Create an Amazon FPGA Image (AFI) From One of The CL Examples: Step-by-Step Guide documentation.


## Opening Existing Vivado Project
Type into TCL console any time reopening the project.

When opening an existing Vivado project (RTL flow), the following TCL command must be run when the project first opens or an error could show up in simulation/implementation flow.

aws::make\_rtl

<a name="rtlnew"></a>
# RTL Project - New RTL Design

Create project directory

start vivado

## Create Vivado Project
aws::make\_rtl

Add RTL sources, sim sources, constraints.

## Opening Existing Vivado Project
Type into TCL console any time reopening the project.

When opening an existing Vivado project (RTL flow), the following TCL command must be run when the project first opens or an error could show up in simulation/implementation flow.

aws::make\_rtl


