# iPhone 16 Pro Max desk stand – organic variant

Built step by step in FreeCAD 1.1 PartDesign (one Body), same phone geometry as `../iphone16promax_stand`:
68° support face (kept straight within 0.25 mm), ledge perpendicular to it, USB-C plug pocket and cable tunnel.

## Design history

1. `Sk_SideProfile` (YZ): two closed B-splines – a flowing side silhouette (lip hook, back rest, swept rear strut) and a side window → `Pad_SideProfile` symmetric 84 mm
2. `Fillet_SoftEdges` 1.5 mm on both silhouettes and window loops
3. `Sk_FlatBottom` (XY) → `Pocket_FlatBottom` 5 mm: trims spline overshoot so the bottom is flat for printing
4. `Sk_PlugPocket` (XY, z = 45) → `Pocket_USBC_Plug` 37 mm
5. `Sk_CableTunnel` (XZ, y = 5) → `Pocket_CableTunnel` through all: cable runs under the window and out the back
6. `Sk_LipNotch` (XZ) → `Pocket_LipNotch` 12 mm, then `Fillet_LipNotch` 1.5 mm

Edit the side shape by moving the B-spline points in `Sk_SideProfile`. Larger fillets (≥ 2 mm) fail on the tightest spline curves (rear foot tip, window apex).

Size 84 x 101 x 122 mm. Print standing on the base, no supports; 3 walls, 15 % gyroid infill.
