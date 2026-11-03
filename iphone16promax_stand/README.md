# iPhone 16 Pro Max desk stand

Modeled interactively in FreeCAD 1.1 (via the FreeCAD MCP addon's RPC server).

- Phone: iPhone 16 Pro Max, 163 x 77.6 x 8.25 mm; slot fits cases up to ~13 mm thick
- Back rest: 68° from horizontal, 105 mm long, 7 mm thick
- Ledge is perpendicular to the back rest so the phone sits flush; front lip 14 mm high with a 40 mm notch (4 mm) so the bottom of the screen stays usable
- USB-C plug pocket (15 x 14 mm) under the phone, 10 x 10 mm cable tunnel exits behind the back rest
- Footprint 90 x 100 mm, height 121 mm, two rear struts

Print lying on the base, no supports needed except optionally the cable tunnel bridge (10 mm, bridges fine). 3 walls, 15–20 % infill.

## Design history (PartDesign Body)

1. `Sk_Base` (XY) → `Pad_Base` 6 mm: 90 x 100 mm base plate
2. `Sk_LedgeLip` (YZ side profile) → `Pad_LedgeLip` symmetric 90 mm: ledge + front lip
3. `Sk_BackRest` (YZ, angle constraint `Tilt` = 68°) → `Pad_BackRest` symmetric 90 mm
4. `Sk_Strut` (YZ, offset x = 24) → `Pad_Strut` 14 mm → `Mirror_Strut` (YZ plane)
5. `Sk_PlugPocket` (XY, z = 45) → `Pocket_USBC_Plug` 39 mm: room for the USB-C plug
6. `Sk_CableTunnel` (XZ, y = 4) → `Pocket_CableTunnel` through all: cable exits at the rear
7. `Sk_LipNotch` (XZ) → `Pocket_LipNotch` 7 mm: lowers the lip in the middle
8. `Fillet_RearCorners` r = 6 mm

Files: `iphone16promax_stand.FCStd`, `iphone16promax_stand.stl`.
