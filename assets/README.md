# Assets: project documentation

`chat-gpt-design-inspiration.png`: the ChatGPT concept image the enclosure was based on.

## `kicad/`

| File | What it shows |
|---|---|
| `01_schematic.png` / `.svg` | Full schematic sheet (kicad-cli render) |
| `02_pcb_layers_front.png` / `.svg` | Front copper, mask, silkscreen and outline plot |
| `03_pcb_copper_front.png` / `.svg` | Front copper and outline only |
| `04_kicad_pcb_editor.png` | PCB editor window |
| `05_kicad_3d_viewer_top.png` | 3D viewer, top view |
| `06_kicad_3d_viewer_perspective.png` | 3D viewer, perspective (OpenGL) |
| `07_kicad_3d_viewer_raytraced.png` | 3D viewer, perspective, raytraced |
| `08_kicad_3d_viewer_bottom_raytraced.png` | 3D viewer, underside with J1, raytraced |
| `09_kicad_schematic_editor_sheet.png` | Schematic editor, whole sheet |
| `10_kicad_schematic_editor_zoom.png` | Schematic editor, zoomed on the circuit |

## `fusion/`: viewport captures (1920x1200)

| # | Topic |
|---|---|
| 01-11 | Whole lamp: iso front/back, orthographic front/back/sides/top, low hero angle, underside with lid |
| 12-16 | Close-ups: PCB in the head, knob with the cable loop, engraved front and back texts, switch |
| 17-23 | Head tilt from -90 to +90 deg (screws and PCB follow the head) |
| 24-25 | Printed parts only / electronics and hardware only |
| 26-28 | X-ray (printed parts at 22 % opacity): iso, side (cable route), front |
| 29-30 | Base with the lid removed: battery holder and cells / empty pocket with foot screws |
| 31-32 | Head without the PCB (brass inserts) / X-ray of the head hardware |
| 33 | View from below |
| 34-38 | Each printed part on its own: head, body, base, lid, tilt screw |
| 39-41 | Visual styles: visible edges, hidden edges, wireframe |
| 42-44 | Component colours (one colour per printed part) |
| 45-47, 52 | Section analysis through the tilt axis: cable channel, loop, hollow screw, threads, foot and base |
| 48-51 | Section analysis front to back: head, PCB, switch, batteries |

### `fusion/renders/`: ray-traced renders (Fusion local renderer)
`R01` Photobooth, `R02` Sharp Highlights, `R03` Warm Light, `R04` Cool Light, `R05` Plaza (outdoor), `R06` Field (outdoor), `R07`/`R08` Photobooth with the light rotated 90 and 180 deg, `R09` Soft Light from behind, `R10` Rim Highlights with the head tilted.

### `fusion/videos/` (MP4 and GIF)
- `timeline_history`: the full Fusion timeline played back step by step (149 steps, captioned)
- `turntable`: 360 deg orbit around the lamp
- `tilt_sweep`: the head tilting through its +/-90 deg range
