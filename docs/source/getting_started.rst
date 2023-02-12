Getting started
===============

Assembly 
----------
Due to the high ammount of components integrated in such small PCB layout, most of them are too small to be soldered at home by you. Therefore, these boards come already 
with the components assembled. 

If you acquired the fully assemble kit, you can skip this section. 

If you selected just the assembled board, you will need to get on your own some other parts to assemble a fully operational |Product|:

- A 2.9" e-paper display. The recommend (and tested working) e-ink panel is the `296x128, 2.9inch E-Ink raw display panel <https://www.waveshare.com/product/2.9inch-e-paper.htm>`_ that you can order directly on the manufacturer. 
  
  Please note that **other displays may not work at all**.
- A :term:`LiPo` battery, with a recommended 1000mAh capacity, for space and power. The ideal dimensions shouldn't excess the 50x34x5mm in order to fit in the designed enclosure.
- An enclosure where to fit the |Product| upper part that you can find on the :ref:`enclosure` section.
- Optionally, you can mount a solar panel that charges the battery under the right sunny conditions. The output voltage of the panel musn't excess the 6V and the recommended size to fit in the designed enclosure is 80x45mm

Powering
--------
The |Product| is be powered through a :term:`LiPo` battery plugged into the white JST connector. The voltage of the battery is reduced to the working 3.3V through a low-consumpiton LDO.

.. Caution::
    Connect the battery after clamping the e-paper connector

In order to charge the battery, there is a battery management IC that provides the right charging curve to the :term:`LiPo` battery and offers a visual indicator (red LED for charging, 
green LED for standby) while the battery is being charged. There are two ways of charging the |Product|: USB-C and solar panel.

USB-C
^^^^^^^^^^^^^
The USB Type-C is a very extended port for portable electronics, and because of it's standarized 5V power supply is ideal for charging the |Product|. Since the battery management IC is designed 
to charge a 1000mAh, there is no need for powerfull USB chargers: any USB-charger capable to deliver 1A will be enough.


Solar panel
^^^^^^^^^^^^^
In addition to the USB-C, and with the aim of extening the service time between (USB) charges of the battery, the |Product| accepts the voltage input (parallel to the USB) from a solar panel.


Sensors
--------
.. figure:: ../../Documentation/Images/SP_Top.png
    :align: right
    :figwidth: 200px
    
As the |Product| is intended to work during long periods of time without having to be recharged, it is important to avoid undesired consumptions 
durint the deep-sleep periods. This implies that the sensors have to be powered **only** when they are needed. 

Therefore there is a high-switch circuit that enables/disables the powering of the *sensors power line* connected to the microcontroller's output **GPIO16**.


Soil moisture
^^^^^^^^^^^^^^
.. figure:: images/getting_started/soil_moisture.png
    :align: left
    :figwidth: 50px
    
Since the |Product| can be directly inserted into the soil of your pot, the area inserted contains a printed circuit that behaves as a 
probe that measures the soil capacity, determined by the soil moisture. As it has no metallic electrodes, there is no risk of probe degradation 
with time. 

The moisture level, in a 0-3.3V range, is measured through the ADC on **GPIO32**

Light sensor
^^^^^^^^^^^^^^^^^^^^^^^
.. figure:: images/getting_started/Illuminance.png
    :align: right
    :figwidth: 300px
    
On the |Product| there is a light sensor consisting on an Everlight's ALS-PT19-315C/L177/TR8, a photodiode sensitive on the range of 
:math:`\lambda = 390...700nm` with the attached response curve.

The illuminance is measured through the ADC on **GPIO33**

.. Hint::
    If you are designing your own enclosure, make sure there is a hole for the light sensor on the case.

Ambient temperature & humidity 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. figure:: images/getting_started/aht20.png
    :align: left
    :figwidth: 100px
The |Product| embeds an AHT20 temperature and humidity sensor ready to deliver calibrated data through the :term:`IIC` (:math:`I^2C`) bus:

:SDA: **GPIO21**
:SCL: **GPIO22**

Battery level
^^^^^^^^^^^^^^^^
The battery is monitored through a very simple circuit that allows the microcontroller directly read the battery's voltage through 
the ADC on **GPIO35**

E-paper
--------

    
The e-ink display pinout with respect to the ESP32 GPIOs goes as follows:
.. figure:: images/getting_started/epaper.png
    :align: right
    :figwidth: 150px

.. list-table:: Pinout table
    :widths: 10 10 
    :header-rows: 1

    * - ESP32
      - E-paper
    * - 25
      - BUSY
    * - 26
      - RST
    * - 27
      - DC
    * - 13
      - CLK
    * - 14
      - MOSI
    * - 15
      - CS

Enclosure
---------
The |Product| PCB can be mounted in a custom :ref:`enclosure` that you can print on your own 3D printer.