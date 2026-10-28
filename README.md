# CMTL 3D Assets

The parts we build instruments out of, already modeled, so you don't have to measure them. Boards, knobs, buttons, jacks, speakers, screens, batteries, plus the cutouts to drop them into an enclosure.

Made for the Creative Music Technology Lab at Georgia Tech. It lives here for now and moves to the CMTL GitHub org soon. Shout out Ben.

## Grab it

Hit the green **Code** button, then **Download ZIP**. That's the whole kit. Want one part? Click the file, then the download button.

Everything is in millimeters.

## Use it

- **Tinkercad:** Import the `.stl`. Need a hole for it? Import the matching file from `08_cutouts`, set it to Hole, and group. Done.
- **Fusion, SolidWorks, Onshape:** Insert the `.step`. Use it as a reference body and design around it.
- **Bambu Studio:** Right-click your model, add a part from `08_cutouts` as a negative part, and you just cut a pocket into a model you didn't even design.

You don't need to design down to the last pixel. Get the outline right, plus the three things that matter: the holes, the ports, and the shafts. Rough everywhere else.

## What's in here

| Folder | What |
| --- | --- |
| `00_design-rules` | The workshop test prints: insert coupon, orientation pair, captured magnet disc |
| `01_brains` | Feathers, QT Pys, RP2040 and RP2350 boards, the MacroPad, ESP32 modules |
| `02_controls` | Pots, the NeoSlider, encoders, NeoKeys, the NeoTrellis, MX and Choc switches, arcade buttons, switches, joysticks, the MPR121 |
| `03_audio-io` | TRS and DC jacks, speakers, I2S and PDM mics, amps, I2S DACs, the MIDI FeatherWing |
| `04_feedback` | NeoPixel rings, sticks, and grids, OLED and TFT screens, haptics |
| `05_sensors` | IMUs, time of flight, gesture, magnetic angle |
| `06_power` | LiPo batteries, chargers, USB-C breakouts, panel mount USB, a STEMMA QT connector |
| `07_hardware` | Heat inserts and magnets as stupid cylinders, to check fits in CAD |
| `08_cutouts` | Ready-to-subtract holes: inserts, magnet pockets, the MX plate cutout, jacks, pots, USB-C, screw clearance |
| `09_enclosures` | Starter boxes with lids, plus Adafruit's QT Py and Pico cases |

Every part folder has an `.stl` for Tinkercad and slicers and a `.step` for real CAD. The one exception is the mini arcade button, which Adafruit only publishes as Fusion files.

## Numbers you'll come back for

**Heat inserts** (CNC Kitchen standard):

| Thread | Hole | Depth to model | Min wall |
| --- | --- | --- | --- |
| M2 | 3.2 mm | 4.0 mm | 1.3 mm |
| M3 | 4.0 mm | 6.7 mm | 1.6 mm |
| M4 | 5.6 mm | 9.1 mm | 2.1 mm |
| M5 | 6.4 mm | 10.5 mm | 2.6 mm |

Iron at your filament's print temp plus 10 to 20 °C. Use an insert tip, let gravity do the work, and stop at flush. Other insert brands need different holes, so check their sheet.

**Fits:**

- Two printed parts that slide: 0.2 to 0.3 mm gap per side
- Screw clearance: screw diameter plus 0.3 to 0.4 mm
- Captured magnet: pocket 0.3 mm bigger across and 0.4 mm taller, with a flat ceiling. Pause at the layer that closes it
- Enclosure walls: 2 mm

Every number here is a starting point. Print a test slice before you print the whole box.

## The workshop props

Print these and pass them around. They make the ideas click.

| File | Shows | Print it with |
| --- | --- | --- |
| `orientation_A_stepped.stl` | A curve facing up turns into stairs | Any nozzle. A 0.8 makes the stairs obvious |
| `orientation_B_smooth.stl` | The same part on its side comes out smooth | Same settings as A |
| `insert_coupon_M2-M5.stl` | Holes for M2 to M5 heat inserts, labeled | A 0.4 nozzle, for accurate holes |
| `magnet_capture_disc_6x3.stl` | A 6 x 3 mm magnet sealed inside | 0.4 nozzle, 0.2 mm layers. Pause at **4.8 mm** |
| `magnet_capture_disc_6x3_0.8nozzle.stl` | Same disc, re-cut for fat layers | 0.8 nozzle, 0.4 mm layers. Pause at **5.2 mm** |

At the pause, drop the magnet in and resume. Mark the polarity first, or you'll seal one in backwards.

## Not in here

- **Seeed XIAO ESP32S3.** Seeed doesn't put a license on its models, so we link instead of copying. They're on the [Seeed wiki](https://wiki.seeedstudio.com/xiao_esp32s3_getting_started/).
- **Everything else Adafruit makes.** This is the music tech greatest hits. The full library is [Adafruit_CAD_Parts](https://github.com/adafruit/Adafruit_CAD_Parts), and if your part isn't here, it's probably there.

## Help wanted

These aren't in any openly licensed library, so we model them ourselves as stupid rectangles plus a cutout:

- [ ] 9 mm Alpha pot (M7 bushing)
- [ ] Slide pot, Bourns PTA style
- [ ] Thonkiconn 3.5 mm jack
- [ ] 1/4 in jack
- [ ] 5-pin MIDI DIN socket

## Add a part

Made something? Add it. Put it in `10_cmtl-originals/your-part-name/` and credit yourself. This is lab history.

1. Millimeters, always. Origin at the center of the mounting face.
2. STEP and STL. Name the folder `vendor_part_variant`, like `cmtl_alpha-9mm-pot`.
3. Add a row to [ATTRIBUTION.md](ATTRIBUTION.md) with the source and license. No source or license, no merge.
4. Every control gets a cutout in `08_cutouts`.
5. Anything you add to `10_cmtl-originals` is shared under CC BY 4.0, same as the rest of our stuff.

## Licensing, in plain words

Remixing with attribution is totally awesome. Here's what you can do with what's in here:

- **Our stuff** (`00_design-rules`, `07_hardware`, `08_cutouts`, the starter boxes, and `10_cmtl-originals`) is [CC BY 4.0](LICENSE). Use it, remix it, even sell it. Just credit CMTL.
- **Adafruit parts** are MIT. Use them for anything. If you share the files, keep Adafruit's notice with them.
- **Espressif modules** are CC BY-SA 4.0 with an exception: anything you design around them is yours. Only edits to the module models themselves have to stay CC BY-SA.
- **kiswitch switches** are MIT or CC BY-SA 4.0, your pick.

Every file's source and license is in [ATTRIBUTION.md](ATTRIBUTION.md), and the full license texts are in [`LICENSES/`](LICENSES). No warranty: if a fit is off, it's the print, not the promise.

The free stuff exists because people made it free. Buy your boards from Adafruit.
