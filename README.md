# Kinesis Advantage

This page summarizes some useful information about Kinesis Advantage keyboards.
Read the [disclaimer](#disclaimer).

## Kinesis Advantage2

### Default controller

The default logic board with the SmartSet 4MiB firmware uses an [Atmel
AT32UC3B0256](https://www.microchip.com/en-us/product/AT32UC3B0256)
microcontroller.

### Alternative controllers

The default SmartSet firmware supports key remappings, macros and even some
support for tap-and-hold. However, the firmware has many limitations compared to
popular open source firmwares like [QMK](https://qmk.fm). For instance, SmartSet
on the KA2 only supports two layers. Some Advantage2 users replace the
controller board to run open source firmware. Replacing the controller is fairly
simple, since the key wells, thumb clusters, and function key rows connect to
the logic board with removable ribbon cables.

The most popular alternative controller is the
[KinT](https://github.com/kinx-project/kint). KinT and QMK support multiple
[Teensy](https://www.pjrc.com/teensy/) microcontroller models. The project also
provides Gerber files to get PCB produced. The maker of the KinT controller has
made a really nice [build video](https://www.youtube.com/watch?v=I0kwQbnhlfk).
If you find building a KinT to daunting, presoldered KinT controllers are often
offered on eBay.

The [KinT Blackpill Edition](https://github.com/dcpedit/kint) is a modification
of the KinT that uses a Blackpill microcontroller with an USB-C connector.

#### USB cable and alternative controllers

Replacement controllers do not have a JST male plug to use the original Kinesis
USB cable. I am not a 100% sure, but I think the issue is that the Teensy
microcontrollers do not break out pins for the USB D+/D- wires. At any rate,
people have used different solutions to this:

* Plug a cable in the Teensy and route it through the USB cable hole. Downsides:
  dust can get in, easy to damage the Teensy.
* Mount a USB panel to the back and plug it in the Teensy. You could even use
  the e-clip of the original cable with this [3D printable
  mount](https://github.com/dcpedit/kinesismod/blob/master/model/kinesis_ush_mount.STL).
  I tried this solution, but unfortunately the e-clip would break the mount.
* Strip a Micro-B cable and [solder a JST male connector to
  it](https://github.com/kinx-project/kint/issues/9#issuecomment-774753427).
  The connector type on the KB600 normally seems to be a 9 pin JST connector
  with 2mm pitch. Advantage: you can use the original KA2 USB cable unchanged.
  Disadvantages: soldering USB wires to a connector with 2mm pitch is difficult;
  very easy to cause shorts between wires.
* Strip a Micro-B cable and the original KA2 USB cable, solder the corresponding
  wires, and isolate (e.g. using masking tape). Disadvantage: modification of
  the original cable, advantage: easier to do safely.

## Kinesis Advantage360

### Default controller

The 360 (SmartSet) uses an [Atmel ATSAMG55J19](https://www.microchip.com/en-us/product/atsamg55) microcontroller.

The 360 Pro (ZMK) version uses a [Holyiot
18010](http://www.holyiot.com/eacp_view.asp?id=278) BLE module with an [Nordic
nRF52840](https://www.nordicsemi.com/products/nrf52840) SoC.

### Teardowns

* [Advantage360](https://photos.google.com/share/AF1QipMO6eK1UNlVNwmLKXALq_Ccbw8jr64TqkqfPVOZEwltHfH8h0rPek8T4rtmxYENIg?pli=1&key=X3g0SDYyOGt6SW14ck1LN1pCeDg3ZlpYOUVQMHNn)
* [Advantage360 Pro](https://imgur.com/a/GZF2vBq)

# Disclaimer

The documentation is provided "as is", without warranty of any kind, express or
implied, including but not limited to the warranties of merchantability, fitness
for a particular purpose and noninfringement. In no event shall the authors or
copyright holders be liable for any claim, damages or other liability, whether
in an action of contract, tort or otherwise, arising from, out of or in
connection with the documentation or the use or other dealings in the
documentation.
