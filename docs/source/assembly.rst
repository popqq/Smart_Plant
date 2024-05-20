🏗️ Assembly
============================

Due to the high amount of components integrated in such small PCB layout, most of them are too small to be soldered at home by you. Therefore, these boards come already 
with the components assembled. 

The |Product|, in addition to the PCB assembled board, consist on the following parts:

- A 2.9" e-paper display. The recommended (and tested working) e-ink panel is the `296x128, 2.9inch E-Ink raw display panel <https://www.waveshare.com/product/2.9inch-e-paper.htm>`_ that you can order directly on the manufacturer. 
  Please note that **other displays may not work at all**.
- A :term:`LiPo` battery, with a recommended 1000mAh capacity, for space and power. The ideal dimensions shouldn't excess the 50x34x5mm in order to fit in the designed enclosure.
- An enclosure where to fit the |Product| upper part that you can find on the :ref:`enclosure` section.
- Optionally, you can mount a solar panel that charges the battery under the right sunny conditions. The output voltage of the panel musn't excess the 6V and the recommended size to fit in the designed enclosure is 80x45mm

In order to assemble your |Product|:

1. Open the clamp connector, by smoothly pulling up the tab.
2. Introduce the e-paper :term:`FPC` with the exposed pads facing up (so that you could still see them)

.. Note::
  The ribbon cable for the e-ink display does not need to be forced in, or slide all the way in. It only goes in a few millimetres, and then the clamp holds it in place.

3. Close the clamp connector

.. Caution::
  Once it's plugged into the |Product|, and without an enclosure, be careful about the e-paper, the connector is fragile and could get damaged if isn't handled with care. It could be useful to use double.sided tape to stuck the screen onto the PCB, just to keep it from flapping loose, but keep in mind that removing it afterwards can damage the e-paper display.

4. Bend carefully the e-paper's :term:`FPC` in a way that the panel rests over the reverse side of the :term:`PCB`.
5. Connect the :term:`LiPo` battery, making sure that the polarity is well respected: red wire is + (positive terminal) and black wire is the - (negative terminal).

At  this point, and without any previous programming, it is normal that the board won't turn on any :term:`LED` or refresh the e-paper; you will need to program it!

Last but not least, make sure you have a fitting enclosure close to you, so you can protect your |Product|. If your printed on of my designs, introduce
the |Product| from the e-paper side connector first before finishing entering the USB-C side.
