# SimpleFOC_G431_Motordriver (24V absolute max)
A motordriver based in STM's G431 Drone ESC

Reason to create it was mainly because of the poor thermal performance of the original development board.
Now the whole "layer sandwich" is gone and every existing layer can breath fresh air.

Additional features

- Two layer design
  ->> The KiCAD file has 2 "blind" layers between top and bottom to test if the additional shielding makes any difference.
      It does not.
      Thos layers can be removed, if you wona make the PCB at home. For JLC price stays almost the same.
      So its still there, because removing it is even less trouble then addin it.

- Exposed Pins
  ->> Thermal sensor and LEDs sadly are gone, so i can stay with in the dimensions i need and keep the two layer design
      But you get new PINs exposed, for additional options (where is lack the skill to add them)

- 36V
  ->> 24V on the original was extreme borderline and came with a high chance to kill it
      The LMR23630 Buck regulator for the first step from VCC to 10V can handle 36V.
      A 60V Version in planned (Parts to change: 

  

      
