# Day 15 – eSim Mixed-Signal Circuit Implementation

## Date
01 October 2026

## Work Completed

- Started practical implementation for the Chapter 1 decision-circuit example.
- Created the `door_lock` Verilog module.
- Verified the Verilog design syntax.
- Generated the NgVeri model from the Verilog design.
- Opened the generated model in KiCad.
- Integrated the digital NgVeri block into a mixed-signal schematic.
- Added pulse sources for the input signals.
- Added ADC bridges for the digital inputs.
- Added a DAC bridge for observing the digital output.

## Circuit Concept

The decision circuit uses two inputs:

- Password
- Authorized

The output `unlock` becomes active only when both conditions are satisfied.

## Current Implementation Flow

Pulse Sources → ADC Bridges → door_lock NgVeri Model → DAC Bridge → Output

## Outcome

A complete mixed-signal schematic for the Chapter 1 decision circuit was prepared in eSim/KiCad.

## Next Step

Configure and run transient Ngspice simulation.