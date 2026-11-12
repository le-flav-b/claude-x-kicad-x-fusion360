# Export: everything needed to build the lamp

## `stl/`: 3D-printed parts (already in print orientation, mm)

| File | Qty | Print orientation | Size (mm) |
|---|---|---|---|
| `lamp_head.stl` | 1 | Back face on the bed (front rim up, insert bosses rise from the back wall) | 44.4 x 41.4 x 20.0 |
| `lamp_body.stl` | 1 | Lying flat on its side | 58.4 x 64.9 x 12.0 |
| `lamp_base.stl` | 1 | Upside down: engraved top on the bed | 66.6 x 66.6 x 20.4 |
| `lamp_base_lid.stl` | 1 | Plate down, snap hooks up | 62.6 x 62.6 x 8.0 |
| `lamp_tilt_screw_x2.stl` | **2** | Knob end on the bed, threaded shank up | 14.0 x 15.7 x 21.0 |

Suggested settings: PLA or PETG, 0.2 mm layers, 0.4 mm nozzle, 4 walls, no supports.
- Tilt screws: 100 % infill. The cable bore leaves about 1.4 mm of wall under the M8 thread, so tighten by hand only.
- Base: high infill if you want a heavier, more stable lamp.
- Thread fit is driven by the `print_clear` user parameter in Fusion (0.2 mm). Raise it and re-export if the screws are too tight.

## `pcb/`: PCB order files (KiCad 10, JLCPCB format)

| File | Use |
|---|---|
| `gerbers_jlcpcb.zip` | Upload this to the PCB order (Gerbers + drill files) |
| `gerbers/` | Same files, unzipped |
| `bom.csv` | Assembly BOM (Designator, Comment, Footprint, Quantity) |
| `cpl_jlcpcb.csv` | Pick-and-place for assembly (D0-D9, R0-R9, J1) |
| `positions.csv` | Raw KiCad position file (includes logo and mounting holes) |
| `schematic.pdf` | Schematic |

Notes:
- 36 mm round board, 2 layers (all routing on F.Cu), 1.6 mm.
- J1 is a through-hole 2-pin header. Hand-solder it, or solder the cable straight to the pads.
- Check LED polarity and rotations in JLCPCB's assembly preview: CPL rotations come straight from KiCad.
- The BOM has no LCSC part numbers. Pick parts at order time: 0805 LEDs, 0805 resistors (adjust the 330 ohm value for your LED colour at 4.5 V).

## `pcb.step`
3D model of the assembled PCB (exported from KiCad, imported into Fusion).

## Hardware

| Part | Qty |
|---|---|
| M2 heat-set insert, M2 x 3, OD 3.2 to 3.6 | 7 (5 head, 2 body foot) |
| M2 x 5 socket head screw (PCB to head) | 5 |
| M2 x 6 socket head screw (base to body foot, from inside the base) | 2 |
| 3xAAA battery holder, 48 x 35 x 13 mm, with leads | 1 |
| AAA cells | 3 |
| Round 2-position ON/OFF switch, 12 mm panel hole, body 12 mm deep max | 1 |
| 2-core cable, 3 mm OD max, about 25 cm | 1 |

## Assembly
1. Melt the 5 inserts into the head bosses and the 2 inserts into the body foot.
2. Route the cable: base pocket, up through the base hole and the foot, along the right arm channel, out under the knob, then through the hollow right tilt screw into the head.
3. Fit the switch in the back of the head. Wire battery+ to the switch, the switch to J1 VIN and battery- to J1 RTN. Solder the wires straight onto J1's pins (there isn't room for a Dupont plug).
4. Screw the PCB onto the head (5 x M2x5).
5. Screw the body onto the base from inside the pocket (2 x M2x6).
6. Put the head between the arms and drive the two tilt screws into the hubs. Their friction holds the tilt angle (+/-90 deg).
7. Drop the battery holder into the pocket and snap the lid on. To open it, hook a finger in the centre hole and pull.
