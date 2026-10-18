# Shot list: ARGUS person-tracking drone article

18 images and 5 videos, all ready in `images/` and `videos/`. Images: 5 drawn by digestdocs as black line art on white (block diagram, flowchart, wiring diagram, components grid, hero), 9 resized from the team's photos in `docs/pics1/`, and 4 frames taken from the team's videos. The drawn ones have an editable `.svg` next to the `.jpg`. Five of the images (6, 12, 13, 17, 18) now serve as the poster frames of the embedded videos (see the Videos table at the end), so they appear in the PDF but not as separate stills on the page.

The article was rewritten as a replication guide: sections follow the build order, and the old week-by-week story is reduced to tips and troubleshooting rows.

All images are 750 px wide or less, JPG, no watermark. If the publishing site has a logo watermark, add it to the three new images only.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `ARGUS-Person-Tracking-Drone.jpg`
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Brief: The drone in its current form (frame with red and white arms, USB webcam at the front, UNO Q visible), on a plain desk or held in the air, with soft daylight and a clean background. `docs/pics1/camera.jpeg` is the closest existing shot but the background is busy. Overlay the title in heavy uppercase type on two lines: "ARGUS" in white or light grey and "PERSON-TRACKING DRONE" in a red accent, top area, clear of the drone. Site logo small at bottom right, if there is one.
- Alt: ARGUS Person-Tracking Drone

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-ARGUS-Person-Tracking-Drone.jpg` (source: `.svg` next to it)
- Size: 750×560
- Section: How Does the ARGUS Person-Tracking Drone Work?
- Note: The dashed line is the planned intent-to-Pixhawk link. Edit the SVG if the camera or companion computer changes.
- Alt: Block diagram of ARGUS person-tracking drone showing USB webcam, Arduino UNO Q, flight intent output, Pixhawk, PDB, ESCs and motors

### 3. Components grid (READY, drawn as line icons; product photos can replace them later)
- File: `Components-Required-for-ARGUS-Person-Tracking-Drone.jpg`
- Size: 750×500, JPG
- Section: Components Required for the ARGUS Drone (above the table)
- Brief: White background, cut-out photos of each part in a grid of 5 + 5, with a bold uppercase label under each: "ARDUINO UNO Q", "RASPBERRY PI 5", "PIXHAWK 2.4.8", "M10 GPS MODULE", "MATEK PDB-XT60", "ESC", "A2212 1000KV MOTOR", "PROPELLER", "USB WEBCAM", "LIPO BATTERY". Add the ESC rating, prop size and battery spec to their labels once known.
- Alt: Components used for ARGUS person-tracking drone including Arduino UNO Q, Raspberry Pi 5, Pixhawk, Matek PDB-XT60, ESCs, brushless motors and USB webcam

### 4. Wiring diagram (READY, drawn black on white; the assumed connections below are drawn as standard wiring)
- File: `Wiring-Diagram-of-ARGUS-Person-Tracking-Drone.jpg`
- Size: 750×500, JPG
- Section: Wiring Diagram of the ARGUS Drone
- Title attribute: Wiring Diagram of ARGUS Person-Tracking Drone
- Brief: Realistic module drawings (Fritzing or Cirkit Designer), light grey background (#E6E6E6), red wires for positive, black for ground, green for signal, a bold black label next to every module. Connections to draw:
  - LiPo battery → XT60 input of the Matek PDB-XT60
  - PDB battery pads → power leads of ESC 1 to 4 *(assumed: confirm the ESCs are wired to the PDB pads)*
  - Each ESC → its brushless motor (3 wires)
  - ESC 1 to 4 signal leads → Pixhawk MAIN OUT 1 to 4, PX4 Quadrotor X order *(assumed: standard PX4 mapping; the logs only say the leads were corrected)*
  - RC receiver → Pixhawk RC input *(assumed: confirm the receiver type and port)*
  - M10 GPS module → Pixhawk GPS port (and I2C port if it has a compass) *(assumed: standard Pixhawk 2.4.8 GPS wiring)*
  - Pixhawk power input → *(TODO: power module or PDB 5V output?)*
  - USB webcam → powered USB hub → Arduino UNO Q USB port
  - Power bank → USB hub power input
  - Arduino UNO Q power → *(TODO: how the UNO Q is powered in flight)*
  - No connection between the UNO Q and the Pixhawk (leave it out, or draw it dashed as "planned")
- Alt: Wiring Diagram of ARGUS Person-Tracking Drone

### 5. Frame CAD design (READY, from `docs/pics1/design2.jpeg`)
- File: `ARGUS-Drone-Frame-CAD-Design.jpg`, 750×422
- Section: Building the ARGUS Frame, under Optional: The 3D-Printed Frame
- Alt: ARGUS drone frame CAD design in Fusion 360 showing the 182 mm bottom plate and four arms

### 6. Printing the centre plate (READY, frame at 0:09 of `docs/pics1/printing.mp4`; poster of video V1)
- File: `3D-Printing-the-ARGUS-Centre-Plate.jpg`, 750×422
- Alt: 3D printing the ARGUS drone centre plate on a Bambu Lab printer

### 7. Printed frame with motors (READY, from `docs/pics1/frame1.jpeg`)
- File: `3D-Printed-Drone-Frame-with-Motors.jpg`, 630×600
- Alt: 3D-printed ARGUS drone frame with lattice arms and four brushless motors mounted

### 8. Failed print (READY, from `docs/pics1/WhatsApp Image 2026-10-09 at 11.46.12 PM.jpeg`)
- File: `Failed-3D-Print-of-Drone-Arms.jpg`, 337×600
- Alt: Failed 3D print of ARGUS drone arms with uneven layers

### 9. Hardware assembly (READY, from `docs/pics1/WhatsApp Image 2026-09-17 at 11.53.48 PM.jpeg`)
- File: `ARGUS-Drone-Hardware-Assembly.jpg`, 750×563
- Alt: ARGUS drone hardware assembly on the quad frame with Pixhawk, ESC wiring and brushless motors

### 10. PDB (READY, from `docs/pics1/pdb.jpeg`)
- File: `Matek-PDB-XT60-Power-Distribution-Board.jpg`, 608×600
- Note: The README captions this photo as the failed PDB, but two electrolytic capacitors are visible on the battery leads, so it may show the board after the fix. The article only describes what is visible.
- Alt: Matek PDB-XT60 power distribution board with soldered ESC and battery leads on the ARGUS drone

### 11. Webcam mounted (READY, from `docs/pics1/camera.jpeg`)
- File: `USB-Webcam-Mounted-on-ARGUS-Drone.jpg`, 750×563
- Alt: USB webcam mounted on the front of the ARGUS drone and connected to the Arduino UNO Q through a USB hub

### 12. QGroundControl calibration (READY, frame at 0:20 of `docs/pics1/calibration.mp4`; poster of video V2)
- File: `QGroundControl-Accelerometer-Calibration-for-ARGUS-Drone.jpg`, 750×422
- Note: This is a photo of the laptop screen. A direct screenshot of the QGC Sensors page would be sharper.
- Alt: QGroundControl accelerometer calibration screen for the ARGUS drone with completed orientations in green

### 13. Motor test (READY, frame at 0:04.5 of `docs/pics1/motor_testinf.mp4`; poster of video V3)
- File: `ARGUS-Drone-Motor-Test-After-ESC-Calibration.jpg`, 338×600
- Alt: ARGUS drone brushless motor spinning during the individual motor test after ESC calibration

### 14. Vision pipeline flowchart (READY, drawn)
- File: `ARGUS-Vision-Pipeline-Flowchart.jpg` (source: `.svg` next to it), 750×1040
- Section: ARGUS Vision Code Explanation
- Alt: Program workflow flowchart of the ARGUS vision pipeline showing frame reading, YOLOv8n detection, tracking, gesture checks and land, hover or follow intents

### 15. Raspberry Pi 5 detection test (READY, from `docs/pics1/WhatsApp Image 2026-09-17 at 11.48.52 PM.jpeg`)
- File: `Raspberry-Pi-5-Person-Detection-Test.jpg`, 450×600
- Alt: Raspberry Pi 5 person detection test showing YOLOv8n bounding boxes with track IDs and JSON intent output in the terminal

### 16. UNO Q dashboard (READY, from `docs/pics1/WhatsApp Image 2026-09-17 at 11.52.14 PM.jpeg`)
- File: `Arduino-UNO-Q-Drone-Vision-Dashboard.jpg`, 750×422
- Note: The screenshot shows a local IP address (192.168.11.101). It is a private LAN address, but crop it out if you prefer.
- Alt: Arduino UNO Q drone vision dashboard showing a tracked person with ID 2, follow action and yaw, forward and vertical intent values

### 17. First flight (READY, from `docs/pics1/WhatsApp Image 2026-09-17 at 11.57.30 PM.jpeg`; poster of video V4)
- File: `ARGUS-Drone-First-Flight.jpg`, 337×600
- Alt: ARGUS drone first flight indoors with the pilot holding the RC transmitter

### 18. Flight with live dashboard (READY, frame at 0:01 of the onboard-camera flight video linked in the README; poster of video V5)
- File: `ARGUS-Week-10-Flight-with-Live-UNO-Q-Dashboard.jpg`, 337×600
- Section: Live Video Demonstration (poster of the onboard-camera flight video)
- Note: Phone video of the laptop screen, so it is soft. A screen recording of the dashboard during a flight would read better.
- Alt: ARGUS drone flying while the Arduino UNO Q dashboard on a laptop shows the onboard camera feed at 0.9 FPS

---

### Videos (READY, team clips)

All five are the team's own clips, transcoded to H.264 MP4 with fast start. In the Markdown they are `<video>` blocks that play the local file first and fall back to the GitHub-hosted original. The demo section also keeps the team's YouTube video (`kJqCdu2nPVA`) as an iframe.

| # | File in `videos/` | Section | Poster | Source |
|---|---|---|---|---|
| V1 | `ARGUS-Printing-the-Centre-Plate.mp4` | Building the ARGUS Frame (optional printed frame) | image 6 | `docs/pics1/printing.mp4` = attachment `8d8be39d…` |
| V2 | `ARGUS-QGroundControl-Calibration.mp4` | Pixhawk Setup, Step 2 | image 12 | `docs/pics1/calibration.mp4` = attachment `80f877c4…` |
| V3 | `ARGUS-ESC-Calibration-and-Motor-Test.mp4` | Pixhawk Setup, Step 3 | image 13 | `docs/pics1/motor_testinf.mp4` = attachment `969b4cbf…` |
| V4 | `ARGUS-First-Flight.mp4` | Live Video Demonstration | image 17 | README attachment `0514c2cd…` |
| V5 | `ARGUS-Flight-with-Onboard-Camera.mp4` | Live Video Demonstration | image 18 | README attachment `bfe29632…` |
