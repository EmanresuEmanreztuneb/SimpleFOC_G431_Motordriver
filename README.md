# SimpleFOC_G431_Motordriver (24V version)
A motordriver based in STM's G431 Drone ESC

Reason to create it was mainly because of the poor thermal performance of the original development board.
Now the whole "layer sandwich" is gone and every existing active layer can breath fresh air.

Changes:

<ins>**Two layer**</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As mentioned, the layer count has been reduced from eight to just two.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The KiCad files still include two "blind" internal layers between top<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;and bottom to test whether additional shielding makes a difference.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;to test if the additional shielding makes any difference.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Spoiler: It doesn’t...<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;You can remove these layers if you plan to etch the PCB at home.<br> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;However, since the price at JLC remains nearly the same, I left them in.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Adding them later would be more effort than simply removing them now.<br>

<ins>**Pins**</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To maintain the required dimensions while sticking to a two-layer design,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;I unfortunately had to remove the thermal sensor and LEDs.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;But you get new pins for your own modifications. (PA15, C10, C11, B5)<br>

<ins>**Stable 24V**</ins> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;On the original version, 24V operation was borderline and carried a high<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;risk of component failure.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The current design uses the LMR23630 for the first stage (VCC to 10V),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;which safely handles up to 36V.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A 60V version is also planned; this will require upgrading to an LMR51635<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;and adjusting the VCC sense resistors.<br>

<ins>**BOOT / Encoder**</ins> <br>
  ->> The BOOT pin is used as Encoder Z, with pull-UP and an additional capacitor.
      This could lead to problems at startup, since the charging time of the capacitor is, what holds PB8 low.
      On the new design, all encoder inputs are pull-DOWN without capacitors.
      This eliminates the use of open collector encoders. But thos are pretty rare Anyway.
      Typical encoders like AMS, CUI, MT6835, 6701 and so on work flawless.

  

  

      
