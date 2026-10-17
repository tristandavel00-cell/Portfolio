
Engineering Specifications

• Primary Input: 110VDC nominal with high-voltage surge protection driven by an LTC4366 controller and an IXTA36N30P MOSFET.
• Intermediate Bus: 12V / 24VDC buck stage driven by an LTC7897 controller.
• Auxiliary Power: Independent +9V (LMR51606 regulator) and +5V (TLV76050 regulator) rails for internal gate drivers and logic.
• Output Stage: 24V/12V 100kHz square-wave switched output driven by an LM5106 half-bridge driver and BUK7Y12-100EX MOSFETs.
• Safety Loop: Low-latency analog overcurrent sensing using a TLV3201 comparator across a 20mΩ shunt.

PCB Layout and Stackup Strategy

The board uses a four-layer stackup to manage high-current paths and isolate noise. The schematic and layout are broken down into clean functional columns:
• Half-bridge top layer (Picture 1): Shows the tight component layout and trace routing for the gate driver and high-power output switching MOSFETs to handle the high-frequency 100kHz square-wave profiles cleanly.
• Top Layer (Picture 2): Contains all the high-voltage lines, low-impedance traces, and tuning circuits. Components are placed as close as possible to the buck-converter stage to minimize loop inductance.
• Bottom Layer (Picture 3): Used as extra space for components that must be near the buck converter when top-layer real estate ran out, as well as general signal routing.
• Layer 3 (Picture 4): Dedicated strictly to low-voltage rails and sensitive signal traces to keep them clear of the high-power switching zones.
• Ground Plane (Picture 5): A dedicated internal reference layer, completely separated from the rest of the routing to reduce high-frequency noise and switching interference.
