# single-stage-opamp-design-using-gpdk180-in-cadence
This repository contains a simple approach to designing a single-stage operational amplifier using gpdk180 in Cadence Virtuoso.

Here's a simple example problem of design:

Design a one-stage Op-Amp that satisfies the following specifications:

| Specification       | Requirement       |
|---------------------|-------------------|
| Power Dissipation   | ≤ 800uW           |
| Gain                | ≥ 30 ± 10%        |
| C Load              | = 5pF             |
| Bandwidth           | ≥ 2MHz            |
| Vout (DC)           | = 2Vdd/3          |

Here is the topology of Single Stage Op-Amp with NMOS drivers and PMOS current mirror load
![image](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/2febc7dc-c7f0-480e-b052-9e6097d50e55)

Now, Let us proceed with Mathematical Calculations:
Here, Vdd = 1.8V
Hence, Vout (DC) = 2 Vdd/3 = 1.2V

![WhatsApp Image 2024-03-25 at 16 58 38_9fbe1eea](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/46a1d395-e13e-4263-9f80-251bf7409bf6)
![WhatsApp Image 2024-03-25 at 16 58 38_6f6f4d17](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/f51f5139-a2fb-4603-880b-93fba9e1a496)

**SIZING M1 & M2 TRANSISTOR (NMOS)**
- Open cadence virtuoso > Click on File > Create New Library > Attach gpdk180 Technology File to it
- Then, Click on file > create Cell view (under that library) > Create Schematic
- Then, use Components to make a setup like given below in the picture for sizing the M1 and M2 transistors.
![1](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/e22d354c-5ca0-49a7-b360-88f88d54d629)

- Now, click on the check and save option and verify in the log that the schematic is saved with no errors
- Then, open ADE L for performing the width sweep
- perform DC sweep on the width variable wn and plot ID of the transistor
![2](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/a3b1e59b-cc73-479c-b186-80e822884cde)
Then, from the above obtained graph, for Id = 170uA (calculated earlier) width of NMOS transistors M1 and M2 comes out to be 12.4u

**SIZING M3 & M4 TRANSISTOR (PMOS)**
- Click on file > create Cell view (under that library) > Create Schematic
- Then, use Components to make a setup like given below in the picture for sizing the M3 and M4 transistors.
![3](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/3726778d-54c9-4611-996b-01398bd4aa49)

- Now, click on the check and save option and verify in the log that the schematic is saved with no errors
- Then, open ADE L for performing the width sweep
- perform DC sweep on the width variable wn and plot "IS" of the transistor
![4](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/20286eff-6acb-4db5-a152-ddb9ac065ea0)

**SIZING M5 TRANSISTOR (NMOS)**
- Click on file > create Cell view (under that library) > Create Schematic
- Then, use Components to make a setup like given below in the picture for sizing the M3 and M4 transistors
![6](https://github.com/afzalamu/single-stage-opamp-design-using-gpdk180-in-cadence/assets/124300839/de39747a-ee9d-4bfb-832e-741330367aa2)
- Now, click on the check and save option and verify in the log that the schematic is saved with no errors
- Then, open ADE L for performing the width sweep
- perform DC sweep on the width variable wn and plot "IS" of the transistor













