# Microprocessor-System-Design

Embedded C and ARM assembly labs on the TI-RSLK MAX robot (MSP432P401R): sensors, timers, motors, interrupts and UART, ending in a line-following, obstacle-avoiding robot (NTU SC2107).

![C](https://img.shields.io/badge/C-embedded-A8B9CC?style=flat-square&logo=c&logoColor=black)
![ARM assembly](https://img.shields.io/badge/ARM-Cortex--M4%20assembly-0091BD?style=flat-square&logo=arm&logoColor=white)
![MSP432](https://img.shields.io/badge/TI-MSP432P401R-CC0000?style=flat-square&logo=texasinstruments&logoColor=white)
![Code Composer Studio](https://img.shields.io/badge/IDE-Code%20Composer%20Studio-CC0000?style=flat-square)
![NTU SC2107](https://img.shields.io/badge/NTU-SC2107%20Microprocessor%20System%20Design-1F3A93?style=flat-square)

## What it does

A Code Composer Studio workspace built on the Valvano "Robot Systems Learning Kit" starter code. Each `LabN_*` folder is a CCS project for one lab; the `*ref_*` folders are the reference examples it builds on.

| Lab | Project | Covers |
|---|---|---|
| 1 | [`Lab1_Assembly`](Lab1_Assembly), [`Lab1_C_Programming`](Lab1_C_Programming) | ARM assembly and C on the MSP432 |
| 2 | [`Lab2_FSM`](Lab2_FSM), [`Lab2_ReflectanceGPIO`](Lab2_ReflectanceGPIO) | Finite state machines (3- and 11-state), GPIO, the reflectance sensor array |
| 3 | [`Lab3_Bump_Reflectance_Systick`](Lab3_Bump_Reflectance_Systick), [`Lab3_TimerCompare_Motor`](Lab3_TimerCompare_Motor) | Bump switches, SysTick, timer compare and PWM motor control |
| 4 | [`Lab4_ADC_IRSensors`](Lab4_ADC_IRSensors), [`Lab4_TimerCapture_Tach`](Lab4_TimerCapture_Tach) | ADC with the IR distance sensors, timer capture with the wheel tachometers |
| 5 | [`Lab5_UARTComms`](Lab5_UARTComms) | UART menu that combines the earlier labs |

Lab 5 combines all four labs, using interrupts, polling, the infrared, reflectance and bumper sensors and the tachometers to follow a line, avoid objects, and calculate wheel RPM from the PWM signal driving both wheels.

## Tech

C and ARM Cortex-M4 assembly, TI MSP432P401R LaunchPad on the TI-RSLK MAX chassis, Code Composer Studio, TExaS display (serial terminal, oscilloscope and logic analyser).

## Run

1. Install [Code Composer Studio](https://www.ti.com/tool/CCSTUDIO) and open this folder as the workspace (or *File > Import > CCS Projects* and pick a lab folder).
2. Build the project; shared drivers come from [`inc/`](inc).
3. Connect the LaunchPad over USB and debug with the target configuration in the project's `targetConfigs/MSP432P401R.ccxml`.

Module documentation is in [`documentation/index.html`](documentation/index.html), datasheets in [`datasheets/`](datasheets) and [`Doc/`](Doc), and the kit's original notes in [`ReadMe.txt`](ReadMe.txt).
