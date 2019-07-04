# Introduction

A laser cutter emits high powered light in order to cut or engrave a target material. Power levels can vary from very small at around or less than 1w through to extremely large at several kw.

This document aims to summarise the hardware options available in considering purchase and maintenance of machines less than 200w as these are the machines most commonly found in hackspaces.

# Machine Beds

One of the biggest factor in determining cost of a machine is the size of bed you wish to work with. Machines can come in any size but it's common to find sizes roughly matching ISO A series paper sizes:

| Designation | ISO Size | Laser bed size |
| --- | --- | --- |
| A0 | 841 x 1189 mm | 900 x 1200mm |
| A1 | 594 x 841 mm | 600 x 900mm |
| A2 | 420 x 594 mm | 400 x 600mm |
| A3 | 297 x 420 mm | 300 x 400mm |
| A4 | 210 x 297 mm | 200 x 300mm |

Machines are sometimes referred to by their rough ISO A series paper size and sometimes as a "6040" or "4060" meaning 600 x 400mm. Be sure you understand the size of the work you expect to cut vs the stated bed size. Beds are normally wider than they are deep. If you're going down the route of building your own machine, you can of course make this any size you want.

When engraving material, the physical bed of our machine does not impact the quality of your results other than potentially depositing resin onto the rear of your piece from previous work. Cutting on the other hand is greatl;y affected by the underlying bed. Each contact with the bed below the work results in reflections that can mark the rear of your work, so it's best to try and minimise these as much as possible.

## Knife or Blade

<a href="https://smokeandmirrors.store/pages/preparing-the-cut"><img src="files/knife-bed.jpg" alt="Knife or blade bed"></a>

Knife beds minimise contact with the work by providing minimal support in the form of vertical knives that the work rests upon. Other than the very top of the knife edge, all edges are angled away from the resting work surface minimising reflections back onto the work above.

The down side of a knife bed is that it can only be used for larger work pieces. Smaller items will drop between the blades when cut through which could then interfere with other cuts or engrave operations.

## Honeycomb

<a href="https://smokeandmirrors.store/pages/preparing-the-cut"><img src="files/honeycomb-bed.jpg" alt="honeycomb bed"></a>

The honeycomb bed design attempts to minimise the contact whilst still providing support to small work. Thin pieces of metal are interlocked to create the structure resulting in the edge of these pieces being in contact and providing a reflection back to the work.

In some cases it may be possible to counteract the flashback by placing paper based masking tape on the rear of the work so that it may absorb the reflections and protect the work. For acrylic, simply leave the protective coating on both sides whilst cutting. When cutting is complete, remove the tape and associated flashback markings.

## Pass through bed

<a href="https://www.businesswire.com/news/home/20180423005466/en/Glowforge-Launches-3D-Laser-Printer-Crowdfunding-History"><img src="https://mms.businesswire.com/media/20180423005466/en/653048/4/Glowforge+Pro+material+in+passthrough+side+view.jpg?download=1"></a>

Some machines feature removable panels or slots in the front and rear of the case allowing larger pieces of work to be placed through the machine whilst the safety and integrity are maintained.

# Motion

Laser cutters are two axis CNC machines with the potential for three in the form of height adjustment. It is relatively uncommon to find machines with the Z axis height adjust controlled by software. In most lower cost machines this motion is provided by a small mains motor and directly switched mains from the control panel.

Additional capacity to work on cylindrical objects may be obtained by replacing one of the axis with a rotary bed.

## Rotary beds

Rotary beds are available in various forms including lathe style chuck or between centres, or via rollers onto which objects can be placed.

Only one of X and Y motion is required during use of a rotary bed - one axis is lined up parallel with your rotary bed path. The stepper driving the tangential path is disconnected and the stepper motor on the rotary bed connects to your stepper drivers instead in order to provide the rotary motion. Most machines have a larger X axis meaning the Y axis is usually the one disconnected to provide motion to the rotary bed.

As with all stepper drivers, take care not to disconnect the motor from a powered stepper driver or damage may result to the driver.

Be sure to calibrate your software for the change to the axis, your step distance is unlikely to be identical between the two different stepper motors.

With all rotary beds you run the risk of damaging your work piece through support rollers, chuck jaws or centre points. Consider this when mounting and either protect the work against this or leave yourself additional material that can be removed in finishing.

### Rollers

Roller style beds can consist of either rollers the full length of your work piece or rollers at either end of your work.

If engraving on to a wine glass, it could be difficult to place the glass onto full length rollers vs rollers only at the ends of the work. Independent rollers at either end of the work can provide greater flexibility in gripping irregularly shaped objects such as a wine glass.

Full width roller style is the cheapest solution to adding rotary motion.

### Chucks

Traditionally found on lathes, small chucks may be used to grip work at one end. Those found for rotary engraving are not usually of the same standard of precision you might find on a lathe as they are not required to spin at any speed. Variants can be found with conventional metal working jaws or more common to woodworking lathes with adjustable pins for differing sizes of work.

Conventional wisdom for metal turning would recommend that the protrusion from the chuck should be no more than three times that of the diameter, though that assumes a sideways force not present in this use case. Use your own judgement in determining if your work needs an additional support such as a live centre at the other end of the work to prevent it becoming off centre during the engrave resulting in non optimal focal length on opposite sides of the work.

### Between centres

Turning between centres is a common operation for both metal and woodworking through the use of a drive centre and either a live (rotating) or dead (stationary) centre at the opposite or tail stock end of the work.

This relatively simple form of drive can provide a high level of accuracy in turning operations but that is not a consideration for this case.

# Laser Source

The most significant decision to make is which laser source to select.  This is the largest cost consideration both in purchase and ongoing maintenance. Laser sources have a limited life and will need to be replaced during the life of the machine.

## Semiconductor

LED lasers have become more common since the advent of blueray disks which brought down the cost of higher powered LED for use in consumer electronics.

The low powered nature of these compared to microwave or CO<sub>2</sub> means these are more suited to engraving than for cutting unless your material is very thin.

LED based machines can go as high as 20w with current technology though it's likely this will increase over time. The laser emitter is usually mounted directly to the gantry of the machine rather than using mirrors on this type of machine so the bed size is usually relatively small.

See also [Wikipedia article on laser diodes](https://en.wikipedia.org/wiki/Laser_diode)

## CO<sub>2</sub>

See also:

* [Comparing glass and metal CO<sub>2</sub> laser tubes](https://uscribe.com.au/knowledgebase/which-is-the-best-glassdc-or-metalrf-co2-laser-tubes/)
* [Which CO<sub>2</sub> laser tube is best?](http://bosslaser.com/blog/2016/02/12/which-co2-laser-tube-is-best-dc-or-rf/)
* [Wikipedia article on gas lasers](https://en.wikipedia.org/wiki/Gas_laser)
* [Wikipedia article on CO<sub>2</sub> lasers](https://en.wikipedia.org/wiki/Carbon_dioxide_laser)

### Glass (DC)

Glass tubes have a relatively low cost to power ratio but suffer from being fragile and of low life in comparison to metal.

Control is in the form of high voltage direct current pulsed through the tube which also contains a water based cooling system.

### Metal (RF)

Metal tubes are high cost and commonly found in industrial settings. Unlike their glass counterpart metal tubes can be refurbished when they do eventually fail resulting in a lower total cost of ownership over the lifetime of a high powered industrial machine in heavy use.

Control is in the form of rapidly pulsed radio frequency energy. Passive cooling is acceptable to around 150w in a moderate climate negating the need for lower power machines to be installed with a water cooling solution.

## Comparison and recommendations

| Source | Spot size | Detail | Typical Life (hours) | Relative Cost | Recommendation |
| --- | --- | --- | --- | --- | --- |
| LED |   | Medium | ~8k | Low | Low cost route into engraving - take care to enclose your machine and protect your eyes |
| Glass CO<sub>2</sub> | ~4mm | Medium | ~10k | Low | Offers best price to power ratio |
| Metal CO<sub>2</sub> | ~2mm | High | ~50k | High | Expensive capital investment but lower cost for high volume use |

## Power Levels

http://am.co.za/laser/thickness

# Electronics (gcode)

Gcode controllers rely on the computer sending the commands to be very specific in it's instructions. See also [Wikipedia G-code](https://en.wikipedia.org/wiki/G-code). All available Open Source controllers make use of gcode to interpret commands from the controlling PC.

## LAOS

Official site: [https://redmine.laoslaser.org/projects/laos/wiki](https://redmine.laoslaser.org/projects/laos/wiki)

* Type of controller:       Open source
* On board stepper drivers: Socketed pololu style
* Support for rotary axis:  No (but can use Y axis)
* Software supported:       Visicut, Corel Draw

Visicut is no longer under active development.

## Smoothieboard

Official site: [http://smoothieware.org/smoothieboard](http://smoothieware.org/smoothieboard)

Smoothieboards are the hardware aspect of the Smoothie project usually paired with [Smoothie](http://smoothieware.org/) firmware to control 3D printers, Laser cutters and CNC machines.

Where to buy: [http://smoothieware.org/getting-smoothieboard](http://smoothieware.org/getting-smoothieboard)

* Type of controller:       Open source
* On board stepper drivers: Yes
* Support for rotary axis:  Yes
* Software supported:       Pronterface, Octoprint, bCNC, Smoopi, Fusion360, Lightburn



## Cohesion3d

Official site: [https://cohesion3d.com/product-category/controllers/](https://cohesion3d.com/product-category/controllers/)

The Cohesion3d board comes in a few varieties.

Smoothie firmware runs on this board.

* Type of controller:       Open source
* On board stepper drivers: Yes
* Support for rotary axis:  Yes
* Software supported:       Lightburn


# Electronics (DSP)

## Ruida

Official site: [http://en.rd-acs.com/](http://en.rd-acs.com/)

Ruida controllers are a commercial off the shelf solution with a huge range of options. This is the most expensive option listed here. For this example we will assume use of 


* Type of controller:       Commercial
* On board stepper drivers: No
* Support for rotary axis:  Yes
* Software supported:       Lightburn



## Stepper Drivers



See also:

* [Arduino forum discussion on adjusting stepper driver current](https://forum.arduino.cc/index.php?topic=415724.0)
* [Hackaday post on Trinamic stepper drivers](https://hackaday.com/2016/09/30/3d-printering-trinamic-tmc2130-stepper-motor-drivers-shifting-the-gears/)


## Power Supply



# Optical Path

In non LED laser machines, there are usually three mirrors to be found and a focusing lense.

Mirror number one is placed at the rear of the machine and reflects the beam from the tube into the body of the machine. Mirror two reflects the beam from the side of the machine along the gantry to the head. Mirror three sits at the top of the head and reflects the beam downwards to the lense and ultimately the work.

<img src="http://www.imajeenyus.com/workshop/20090506_laser_cutter/beam_alignment_photos/optics_path.jpg" width="602" height="480" />

Image linked from [Beam alignment article from Lindsay Wilson](http://www.imajeenyus.com/workshop/20090506\_laser\_cutter/beam\_alignment.shtml)

## Mirrors

The science behind optical reflectivity is deep and extensive. Mirrors are usually 20mm or 25mm diameter though are available in other diameters. Mirrors are made either from a solid piece of material or by applying a coating to another material.

Key indicators to note are optical reflectivity, divergence from perfectly flat and surface finish. Different materials, reflective coatings and protective coatings will also behave differently depending on the optical wavelength of your laser source.

Key performance indicators for mirrors are:

| Value | Unit | Notes | Guide value |
| --- | --- | --- | --- |
| Reflectance | Percentage | Larger is better | &gt;= 99% |
| Surface flatness | Fractions of wavelength | Smaller is better | lambda/4 @ 1064 nm |
| Surface quality | scratch-dig | Smaller is better | 40-20 or less |

A protective coating applied to any mirror will prolong it’s operating life and make damage less likely in the course of use and cleaning.

### K9 - Glass

K9 mirrors are glass with a gold coating on one face. A coating is applied to protect the gold from oxidation.

Due to the base material used, thermal conductivity is low resulting in all heat being dissipated in the reflective and protective coatings. They are not suitable for use with CO<sub>2</sub> lasers greater than 50w due to their lack of thermal mass.

These mirrors are cheap, low quality and fragile. They are also prone to overheating and the coating catching fire if the mirror is in any way dirty. Avoid this type of mirror.

### Si - Silicon Glass

Si mirrors are silicon infused glass with a gold coating on one face. A coating is applied to protect the gold from oxidation.

These mirrors are typically rated up to 150w for use with CO<sub>2</sub> lasers. These are recommended as the default for hobbyists operating home machines. A base material of glass makes these fragile.

### Mo - Molybdenum

Mo mirrors are molybdenum polished to a high finish, as a result these mirrors are silver in colour rather than the gold of all of the others discussed in this document.

There is usually no reflective or protective coatings on this material. It's extremely hard wearing and is recommended for hackspace or high use machines.

These mirrors appear to be rated up to 200W for use with CO<sub>2</sub> lasers.

### Cu - Copper

Cu mirrors are a solid copper base material with a gold coating on one face. A coating is applied to protect the gold from oxidation.

These mirrors are rated at a similar power level to Mo at 30-200W for CO<sub>2</sub> lasers. They are the best heat absorbing mirror for higher power optical paths however they typically have a lower reflectance and surface quality due to the softer base material.

The most expensive of the mirrors we have looked at here, they are liable to scratching if not maintained with great care.

### Comparison and recommendations

The following values are based on research of mirrors available via Aliexpress and other online vendors of mirrors. The figures may be inaccurate or misleading and you are encouraged to do your own research. Values supplied are typical for the mirrors found.

| Material | Reflectance | Flatness | Quality | Power | Recommendation |
| --- | --- | --- | --- | --- | --- |
| K9 |  | &Lambda;/2 per 1" diameter @ 10.6&micro;m | 40-20 | 30w - 50w | Poor quality - don't use these |
| Si |  | &Lambda;/2 per 1" diameter @ 10.6&micro;m | 40-20 | Up to 200w | Ideal middle ground for home and hobby machines |
| Mo |  | &Lambda;/2 per 1" diameter @ 10.6&micro;m | 40-20 | Up to 200w | Hard wearing in tough environments - ideal for hackspace machines |
| Cu |  | &Lambda;/2 per 1" diameter @ 10.6&micro;m | 60-40 | Up to 200w | Ideal for higher power machines 120w or greater? |

The science of mirrors is extensive and complicated, most of which is not relevant to the purchase of mirrors for laser cutters.

As a general guide, better quality mirrors cost more and are better packed for shipping but that's often hard to determine from the details given in an online listing. American manufactured mirrors are usually the best quality. If this seems vague, you are correct. Differentiation between mirrors is difficult unless you're willing to pay top price for scientific specification mirrors.

## Lenses

## Hardware around optics

## Alignment

## See also

* [Sawmill Creek - forum discussion of mirrors](https://sawmillcreek.org/showthread.php?206087-Mirror-types-for-CO2-lasers&p=2138204#post2138204)

* [Photonics - Mirrors: Coating choice makes a difference](https://www.photonics.com/Articles/Mirrors\_Coating\_Choice\_Makes\_a\_Difference/a25501)

* [Edmund Optics - Understanding optical specifications](https://www.edmundoptics.com/resources/application-notes/optics/understanding-optical-specifications/)

* [Metallic mirror coatings](https://www.edmundoptics.com/resources/application-notes/optics/metallic-mirror-coatings/)

* [RMI Co Optics tutorial](http://rmico.com/optics-tutorial)

* [Metallic Reflection](https://eng.libretexts.org/Textbook_Maps/Chemical\_Engineering/Supplemental\_Modules\_\(Materials_Science\)/Optical\_Properties/Metallic\_Reflection)

* [Reflection \(Physics\)](https://en.wikipedia.org/wiki/Reflection_\(physics\))

* [Directed Light CO<sub>2</sub> mirrors](http://directedlight.com/laser-components/catalog/co2-mirrors/)

# Red dot indicator

* [Article from Martin](https://msraynsford.blogspot.com/2018/10/beam-combiner-vs-head-mounted.html)

## Head mounted

## Beam combiner

# Water Cooling

## Barrel of water

## Passive chiller

## Active chiller



# Air assist

Air assist serves to clear smoke away from your cutting head as quickly as possible. This both keeps the smoke away from your lense reducing cleaning frequency but also clearing smoke in the optical path to the work preventing unpredictable changes in power due to attenuation.

There are two common approaches to providing the air supply to discuss.

## Linear Compressors

<img src="./media/image1.png" width="225" height="225" />

Attribution for image - taken from the old Just Add Sharks site - need to ask Dominic/Martin if it’s okay to use it.

Flow rates? Does cutter size matter or is it about power levels?

See also:

* [AvE video on linear compressors](https://www.youtube.com/watch?v=eEF-owkyI-o)

* [Wikipedia Linear Compressor](https://en.wikipedia.org/wiki/Linear\_compressor)

## Tooling Compressors

Traditional compressors intended for use driving air tools usually provide up to 150psi.

Efficiency

Water issues.

See also:

* [Wikipedia Compressor page](https://en.wikipedia.org/wiki/Compressor)

# Extraction

## Flow rates & size

## Noise

## Options

# Connectivity

## USB

## Ethernet

## Wireless

# Software

## Lightburn

## Lasercut

## What else?

# Maintenance

## Mirrors

## Lense

## Bed & housing

## Ways and slides

## Z axis

## Interlocks

Varify correct operation of all interlocks?

## Chiller

Water changes

Additives

Protection against freezing

# Appendix 1 - Safety

## Beams

Lasers emit sometimes invisible optical radiation that can seriously damage your eyesight. Don’t look directly into the beam or it’s reflections.

## Materials

Be careful what you cut/etch. Not all materials are suitable and many can give off poisonous gasses when cut using a laser. If in doubt, make sure that you purchase laser safe supplies from a reputable supplier.

The London Hackspace has an excellent wiki article detailing how to [identify if an unknown material is safe to cut](https://wiki.london.hackspace.org.uk/view/Silvertail_A0_Laser_Cutter#List_of_allowed_and_banned_materials)

# Appendix 2 - Mirror Science

# Appendix 3 - Lense Science

# Case Studies

* [Mirrors - examining a sample](Case%20study%20-%20mirrors.md)

* [Manchester Hackspace (Hacman) - purchase and maintenance of A2 laser](Case%20study%20-%20Hacman-A2.md)

# See also

* [Sarbar Multiedia](https://www.youtube.com/user/SarbarMultimedia/videos)
