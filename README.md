# claude-x-kicad-x-fusion360

A tiny product I made to test AI capabilities with specific design softwares like KiCad and Fusion360.

Ten LEDs in a ring on a 36 mm round board, each with its own 330 Ω series
resistor, all fed from a single 2-pin header. The whole thing — schematic,
ERC, layout, placement, routing, copper pours, DRC and 3D export — was built
by driving KiCad through the Konnect MCP server.

## The board

- 36 mm circular outline, four arcs, no straight edges
- Single copper layer: everything routes on F.Cu
- 10 × LED_0805 on a 14 mm radius ring, 10 × R_0805 on an 8 mm radius ring,
  all oriented radially at 36° steps
- D0 sits to the left of the connector, numbering runs clockwise to D9
- VIN is distributed by an inner copper pour (8 mm radius); RTN is a ground
  pour filling the rest of the board. Between them the two pours carry every
  power connection, so the only traces on the board are the ten radial
  branches plus the connector's VIN feed
- Decorative sun in the centre: 20 silkscreen rays, the ten on the component
  axes shorter than the ten between them
- 5 × M2 mounting holes for attaching to a 3D-printed enclosure
- J1 renders on the underside in the 3D view

## Files

| File | What it is |
| --- | --- |
| `claude-x-kicad-x-fusion360.kicad_sch` | Schematic |
| `claude-x-kicad-x-fusion360.kicad_pcb` | Board layout |
| `pcb.step` | 3D export |
| `sunlogo.pretty/` | Footprint library holding the sun logo |

## Status

ERC: 0 errors, 0 warnings.
DRC: 0 errors, 0 warnings, 0 unconnected items.
