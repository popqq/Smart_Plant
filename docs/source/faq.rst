:term:`FAQ`
=============================

After connecting everything and turning on the |Product|, I don't see the e-paper refresh or any LED on.
    This probably means that your |Product| run out of battery. Charge the battery, you will see the red LED on that will turn green when finishes. 

Can I upload ESPHome directly from the Home Assistance setup running on my Raspberry Pi?
    Yes you can, and actually this is one of the simplest and more effective way to upload ESPHome.

Can I upload firmware through the USB-C?
    No, at the moment the USB-C can only be used for charging the battery.

When I try to compile the given YAML and upload it into the board I get some error messages saying that I miss some files (Audiowide.ttf, icon-map.h, etc). How to fix it?
    Just the configuration YAML file isn’t enough and you might get an error asking for missing items (the fonts and the images). The reason is because
    on the configuration we are asking for some files (the fonts that you want for the digits or the icons and the background image with the plant and the gauges).
    
    Therefore you need to upload into the folder with the configuration YAML file the required files. I strongly suggest to use Visual studio code and just drag and 
    drop the items according to the structure mentioned on the :ref:`esphome` programming section.