# Shot list: ResQmesh micro quadcopter article

9 images and 3 team videos in article order, plus the team's YouTube video, all ready in `images/` and `videos/`:

- 5 images drawn by digestdocs: hero, block diagram, flight-loop flowchart, components grid and circuit diagram. Four are black line art on white, and the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 4 images made from the team's own pictures, which are GitHub attachments in the weekly logs: the KiCad motor-driver screenshot, the printed frame, the driver-board strip (three photos joined) and the assembled drone.
- 3 videos from the weekly logs, transcoded to H.264 MP4 with a poster JPG each. In the Markdown they are `<video>` blocks that play the local file first and fall back to the GitHub-hosted original. In the PDF each one shows its poster frame and a link.
- The Live Video Demonstration section embeds the team's YouTube video (`m4jHtg0Pzuk`, "ResQmesh - Lightweight ESP32-based Drone Swarm | Builder in Residence", TinkerHub Foundation), which is an interview with the two builders.

The article is a replication guide (parts, wiring, frame printing, assembly, flashing, bench tests), so media sit under the build step they illustrate.

Left out on purpose: the Week 5 KiCad session photo and the soldering portrait (both mainly show people), and three README images that duplicate log photos.

All images are 750 px wide or less, JPG, no watermark.

---

### 1. Featured hero image (READY, drawn)
- File: `ResQmesh-ESP32-Micro-Quadcopter.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field
- Note: the two follower quads are dashed and labelled "planned", as the swarm has not been tested. A photo version could use the Week 9 assembled-drone photo (`8f0e7eab…`) with the title overlaid.
- Alt: ResQmesh ESP32 Micro Quadcopter

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-ResQmesh-Micro-Quadcopter.jpg` (source: `.svg`)
- Size: 750×470
- Section: How Does the ResQmesh Micro Quadcopter Work?
- Note: dashed boxes are the handheld ESP32 transmitter (firmware in `code/ESP32-CONTROLLER`) and the ESP-NOW followers, both written in code but not tested.
- Alt: Block diagram of ResQmesh micro quadcopter showing phone, GY-9250 IMU, XIAO ESP32-S3, AO3400A motor switches, 720 coreless motors, 1S LiPo and planned ESP-NOW followers

### 3. Flight-loop flowchart (READY, drawn)
- File: `ResQmesh-Flight-Loop-Flowchart.jpg` (source: `.svg`)
- Size: 750×1050
- Section: How Does the ResQmesh Micro Quadcopter Work?
- Source: `firmware/flight_controller.cpp`, `safety.cpp`, `mixer.cpp` (750 ms link timeout and 60° tilt limit from `config.h`)
- Alt: Flowchart of ResQmesh 500 Hz flight loop with link check, arming check, cascaded PID, motor saturation check and 20 kHz PWM output

### 4. Components grid (READY, drawn as line icons)
- File: `Components-Required-for-ResQmesh-Micro-Quadcopter.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required (above the table)
- Brief for a photo version: white background, cut-out photos in a 5 + 5 grid, labels "XIAO ESP32-S3", "GY-9250 IMU", "720 MOTOR ×4", "55 mm PROP ×4", "AO3400A ×4", "1N5819 ×4", "470µF CAPACITOR", "1S LIPO", "PERFBOARD", "3D-PRINTED FRAME".
- Alt: Components required for ResQmesh micro quadcopter including XIAO ESP32-S3, GY-9250 IMU, 720 coreless motors, 55 mm propellers, AO3400A MOSFETs, 1N5819 diodes and 1S LiPo

### 5. Circuit diagram (READY, drawn black on white)
- File: `Circuit-Diagram-of-ResQmesh-Micro-Quadcopter.jpg` (source: `.svg`)
- Size: 750×640, JPG
- Section: Circuit Diagram of the ResQmesh Micro Quadcopter
- Title attribute: Circuit Diagram of ResQmesh Micro Quadcopter
- Connections and their sources:
  - Motor pins GPIO4, GPIO1, GPIO2, GPIO3 (pads D3, D0, D1, D2): `firmware/config.h`; the KiCad schematic also puts the motors on D0 to D3.
  - I2C SDA GPIO5 (D4), SCL GPIO6 (D5): `config.h` and the Week 8 log; 4.7kΩ pull-ups from the Week 8 log.
  - Per channel: 100Ω gate resistor, 100kΩ gate pull-down, 1N5819 across the motor, 100nF across the motor tabs: KiCad schematic, board photo (resistor bands brown-black-yellow) and the Week 5 log.
  - 470µF across the battery and star ground at LiPo −: Week 5 and Week 9 logs.
  - XIAO powered through its BAT+ back pad: from the note in `firmware/config.h` *(inferred from that comment; confirm)*.
  - Battery divider: not drawn, because `BATTERY_MONITOR_ENABLED` is 0 in the flashed firmware.
- Brief for a Fritzing/EasyEDA version: light grey background, realistic XIAO and GY-9250 drawings, red = +, black = GND, green = signal, all four channels drawn out.

### 6. KiCad motor-driver screenshot (READY, from the team's image)
- File: `ResQmesh-KiCad-Motor-Driver-Schematic.jpg`
- Size: 540×437 (native)
- Section: Circuit Diagram
- Source: Week 5 log (`7cc1ad72…`)
- Alt: KiCad schematic of one ResQmesh motor driver channel with 720 motor, 1N5819 diode, AO3400A MOSFET, 100 ohm gate resistor and 100 kilo-ohm pull-down

### 7. Printed frame (READY, from the team's photo)
- File: `3D-Printed-ResQmesh-Unibody-Frame.jpg`
- Size: 750×500, JPG
- Section: 3D Printing the ResQmesh Frame
- Source: Week 2 log (`5a3657c1…`), cropped to 3:2
- Alt: 3D-printed ResQmesh unibody quadcopter frame on the printer bed

### 8. Driver board strip (READY, from the team's photos)
- File: `ResQmesh-Hand-Wired-MOSFET-Driver-Board.jpg`
- Size: 750×360, JPG
- Section: Assembling the ResQmesh Micro Quadcopter, Step 1 (driver board)
- Source: Week 9 photos `d6052a8d…` (diodes and 100kΩ resistors), `efbc844c…` (four SOT-23 MOSFETs) and Week 6 photo `a9a54c20…` (board on the GY-9250)
- Alt: ResQmesh hand-wired driver board with 1N5819 diodes and 100 kilo-ohm resistors, four AO3400A SOT-23 MOSFETs, and the board stacked on the GY-9250 IMU

### 9. Assembled drone (READY, from the team's photo)
- File: `Assembled-ResQmesh-Micro-Quadcopter.jpg`
- Size: 750×600, JPG
- Section: Assembling the ResQmesh Micro Quadcopter, Step 4 (stack the boards)
- Source: Week 9 log (`8f0e7eab…`)
- Alt: Assembled ResQmesh micro quadcopter with XIAO ESP32-S3 and GY-9250 IMU stacked on the driver board, 720 coreless motors and 55 mm propellers

### Videos (READY, team clips)

| # | File in `videos/` | Section | Source |
|---|---|---|---|
| V1 | `ResQmesh-Soldering-the-Driver-Board.mp4` | Assembly, Step 1 | Week 6, `fb0bdad3…` (no audio) |
| V2 | `ResQmesh-Motor-Spin-Test.mp4` | Output | Week 9, `4e7536c5…` |
| V3 | `ResQmesh-Hand-Test-Counter-Torque.mp4` | Output | Week 10, `9f020abd…` |
| YT | YouTube `m4jHtg0Pzuk` | Live Video Demonstration | README |

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links filled.
