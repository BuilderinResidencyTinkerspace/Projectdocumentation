# Shot list: CuBaffle deployable CubeSat optical baffle article

10 images in article order, all ready in `images/`, plus the demo video still to make (item 11):

- 5 drawn by digestdocs: hero, block diagram, flowchart, components grid and circuit diagram. All are on white; four are black line art, and the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 5 made from the photos and the screenshot attached to the weekly logs (GitHub user-attachments): the sketches, the acrylic chassis, the printed stages, the nested/extended pair and the dashboard.

The repository has no videos, so nothing could be embedded. The CubeSat Design Specification drawing in the Week 4 log is a third-party figure and was left out.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `CuBaffle-Deployable-CubeSat-Optical-Baffle.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Brief for a photo version: the acrylic 1U chassis on a plain desk with the baffle deployed, Pi and servos visible through the clear walls, soft daylight. Title in heavy uppercase on two lines, "CUBAFFLE" in white and "DEPLOYABLE OPTICAL BAFFLE" in a red accent, top area, clear of the cube.
- Alt: CuBaffle Deployable CubeSat Optical Baffle

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-Deployable-CubeSat-Optical-Baffle.jpg` (source: `.svg`)
- Size: 750×420
- Section: How Does the Deployable CubeSat Optical Baffle Work?
- Alt: Block diagram of the deployable CubeSat optical baffle showing Raspberry Pi 5, Pi Camera Module 3, MG90S servos, 3-stage baffle, 4xAA servo battery and Wi-Fi dashboard

### 3. Dashboard program flowchart (READY, drawn)
- File: `CuBaffle-Dashboard-Program-Flowchart.jpg` (source: `.svg`)
- Size: 750×900
- Section: How Does the Deployable CubeSat Optical Baffle Work?
- Note: values from `code/baffle_phase3.py` (2300/1600 µs, 2.5 s ramp, 0.3 s settle, HTTP 409 when busy).
- Alt: Flowchart of the CuBaffle dashboard program showing startup stow, button commands, busy and state checks, smoothstep servo ramp, frame capture and glare comparison

### 4. Components grid (READY, drawn as line icons; product photos can replace them later)
- File: `Components-Required-for-Deployable-CubeSat-Optical-Baffle.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required (above the table)
- Brief for a photo version: white background, 4 + 4 grid, bold uppercase labels: "RASPBERRY PI 5", "PI CAMERA MODULE 3", "MG90S SERVO ×2", "4×AA BATTERY HOLDER", "PI 5 POWER SUPPLY", "2.88 mm ACRYLIC SHEET", "3D PRINTER FILAMENT", "PERF BOARD".
- Alt: Components required for the deployable CubeSat optical baffle including Raspberry Pi 5, Pi Camera Module 3, MG90S servos, 4xAA battery holder, acrylic sheet and 3D printer filament

### 5. Circuit diagram (READY, drawn black on white)
- File: `Circuit-Diagram-of-Deployable-CubeSat-Optical-Baffle.jpg` (source: `.svg`)
- Size: 750×520, JPG
- Section: Circuit Diagram of the Deployable CubeSat Optical Baffle
- Title attribute: Circuit Diagram of Deployable CubeSat Optical Baffle
- Connections drawn (Week 8 log and README):
  - Both MG90S signal leads → perf board → Pi pin 32 (GPIO12, PWM0)
  - Both servo V+ → 4×AA pack + (6V); both servo GND → pack − → Pi pin 39
  - Pi 5 → official power supply (USB-C); Pi Camera Module 3 → camera connector (ribbon)
  - Pin 33 (GPIO13, PWM1) is driven by the code but shown unconnected, as the log wires both servos to pin 32
- Brief for a Fritzing/Cirkit version: light grey background, realistic modules, orange signal, red 6V, brown/black ground, bold labels.

### 6. Baffle and servo arm sketches (READY, from the Week 5 photos)
- File: `CuBaffle-Baffle-and-Servo-Arm-Sketches.jpg`
- Size: 750×480, JPG
- Section: Designing the Telescoping Baffle
- Source: Week 5 sketches `f12fbdf4…` (stowed side view, lower plate top view, upper plate bottom view) and `c0e405b8…` (deployed side view), cropped side by side with labels
- Alt: CuBaffle baffle and servo arm sketches showing the stowed side view, the lower and upper plates with servos and arm grooves, and the deployed side view

### 7. Laser-cut acrylic chassis (READY, from the Week 4 photo)
- File: `Laser-Cut-Acrylic-1U-CubeSat-Chassis.jpg`
- Size: 750×600, JPG
- Section: Building the 1U CubeSat Chassis
- Source: `fa64e68c…`
- Alt: Laser-cut transparent acrylic 1U CubeSat chassis with finger joints for the deployable optical baffle

### 8. Printed telescoping stages (READY, from the Week 8 photo)
- File: `3D-Printed-Telescoping-Baffle-Stages.jpg`
- Size: 600×750, JPG
- Section: 3D Printing and Assembly of the Baffle
- Source: `2b18a011…`
- Alt: 3D-printed telescoping baffle stages with the top plate and slotted rails for the deployable CubeSat optical baffle

### 9. Nested and extended in the chassis (READY, from two Week 8 photos)
- File: `CuBaffle-Baffle-Nested-and-Extended-in-1U-Chassis.jpg`
- Size: 750×480, JPG
- Section: 3D Printing and Assembly of the Baffle
- Source: `daf272ca…` (nested in the chassis) and `86e4c5b2…` (stages extended by lifting the top), side by side with labels
- Alt: CuBaffle telescoping baffle nested inside the acrylic 1U CubeSat chassis, and the three stages extended by lifting the top

### 10. Dashboard Control tab (READY, from the Week 9 screenshot)
- File: `CuBaffle-Web-Dashboard-Control-Tab.png`
- Size: 750×235, PNG (flat UI screenshot)
- Section: Output: Testing the Deployable CubeSat Baffle
- Source: `4b18fa8a…`, cropped to the buttons and log. The full-resolution log shows nine deploy/stow cycles between 01:20 and 01:46.
- Still to shoot: an Analysis tab screenshot (stowed, deployed and difference images with the verdict line) once the baffle is reprinted in matte black.
- Alt: CuBaffle web dashboard Control tab showing STOW and DEPLOY buttons, state STOWED and the live system log

### 11. Demo video (TO MAKE)
- Section: Live Video Demonstration (YouTube embed with `VIDEO_ID`)
- Suggested shots: the cube on a desk with the dashboard on a phone beside it; Deploy and Stow pressed, showing the 2.5-second smoothstep motion through the clear acrylic; the Live Feed tab; the Analysis tab result.

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
