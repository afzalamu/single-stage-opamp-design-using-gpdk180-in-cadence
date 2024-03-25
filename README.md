# single-stage-opamp-design-using-gpdk180-in-cadence
This repository contains a simple approach to designing a single-stage operational amplifier using gpdk180 in Cadence Virtuoso.

Here's a simple example problem of design:

Design a one stage Op-Amp that satisfies following specifications:

| Specification       | Requirement       |
|---------------------|-------------------|
| Power Dissipation   | ≤ 800uW           |
| Gain                | ≥ 30 ± 10%        |
| C Load              | = 5pF             |
| Bandwidth           | ≥ 2MHz            |
| Vout (DC)           | = 2Vdd/3          |

Here is the topology of Single Stage Op-Amp with NMOS drivers and PMOS current mirror load
![image](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/2febc7dc-c7f0-480e-b052-9e6097d50e55)

