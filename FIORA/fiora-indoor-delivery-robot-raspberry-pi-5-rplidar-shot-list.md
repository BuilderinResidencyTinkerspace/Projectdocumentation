# Shot list: FIORA indoor delivery robot article

12 images and 1 video in article order, all ready in `images/` and `videos/`:

- 5 images drawn by digestdocs: hero, block diagram, planned delivery workflow flowchart, components grid and wiring diagram. Four are black line art on white, and the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 7 images made from the team's photos, which are GitHub attachments in the weekly logs: two of them are strips that join several photos with arrows.
- 1 video: the Week 7 mapping run, transcoded to H.264 MP4 (fast start) with a poster JPG. In the Markdown it is a `<video>` block that plays the local file first and falls back to the GitHub-hosted original. In the PDF it shows its poster frame and a clickable link.

All images are 750 px wide or less, JPG, no watermark. If the publishing site uses a logo watermark, add it to the drawn images only.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `FIORA-Indoor-Delivery-Robot.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Brief for a photo version: the round prototype body on the TinkerSpace floor with the RPLIDAR A1M8 on top, three-quarter view, soft light. Title in heavy uppercase on two lines, "FIORA" in white and "INDOOR DELIVERY ROBOT" in a red accent, top area, clear of the robot.
- Alt: FIORA Indoor Delivery Robot


### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-FIORA-Indoor-Delivery-Robot.jpg` (source: `.svg`)
- Size: 750×660
- Section: How Does the FIORA Indoor Delivery Robot Work?
- Note: Dashed boxes and arrows are planned (Telegram bot, Pi-to-Arduino motion link).
- Alt: Block diagram of FIORA indoor delivery robot showing RPLIDAR A1M8, Raspberry Pi 5 with ROS 2, RViz2, HC-05, Arduino Uno with L293D shield, GB37 motors and mecanum wheels


### 3. Planned delivery workflow flowchart (READY, drawn)
- File: `FIORA-Planned-Delivery-Workflow-Flowchart.jpg` (source: `.svg`)
- Size: 750×870
- Section: How Does the FIORA Indoor Delivery Robot Work?
- Note: Redrawn from the "Intended delivery workflow" Mermaid chart in the README. The brackets mark the two steps that work today and the planned rest.
- Alt: Flowchart of the planned FIORA delivery workflow from power-on and LiDAR start-up to map loading, delivery request, route planning, obstacle checks and user notification


### 4. Components grid (READY, drawn as line icons; product photos can replace them later)
- File: `Components-Required-for-FIORA-Indoor-Delivery-Robot.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required for the FIORA Indoor Delivery Robot (above the table)
- Brief for a photo version: white background, cut-out photos in a 5 + 5 grid, bold uppercase label under each: "RASPBERRY PI 5", "RPLIDAR A1M8", "ARDUINO UNO", "L293D MOTOR DRIVER SHIELD", "HC-05 BLUETOOTH", "GB37 12V MOTOR ×4", "MECANUM WHEEL ×4", "LIPO BATTERY", "POWER BANK (PI SUPPLY)", "3D-PRINTED COUPLER + MOUNT". Add the battery voltage to its label once known.
- Alt: Components required for FIORA indoor delivery robot including Raspberry Pi 5, RPLIDAR A1M8, Arduino Uno, L293D motor driver shield, HC-05, GB37 motors and mecanum wheels


### 5. Wiring diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-FIORA-Indoor-Delivery-Robot.jpg` (source: `.svg`)
- Size: 750×640, JPG
- Section: Wiring Diagram of the FIORA Indoor Delivery Robot
- Title attribute: Wiring Diagram of FIORA Indoor Delivery Robot
- Connections drawn from the logs and photos:
  - RPLIDAR A1M8 → USB adapter board → Raspberry Pi 5 USB (Week 6 log, photos)
  - Power bank → Raspberry Pi 5 USB-C (Week 8 log)
  - L293D Motor Driver Shield stacked on the Arduino Uno, four GB37 motors on M1 to M4 (Week 5 log)
  - HC-05 to the Arduino (Week 5 log) *(assumed: which serial pins; drawn dashed)*
  - LiPo to the shield's EXT_PWR terminal *(assumed: the logs only say the battery was mounted with the electronics; drawn dashed)*
  - Motor-to-terminal order *(not recorded)*; encoder leads not drawn
- Brief for a Fritzing/Cirkit version: light grey background (#E6E6E6), realistic module drawings, red = +, black = GND, green = signal, bold label next to each module.


### 6. Base and motor-mount build steps strip (READY, from the team's photos)
- File: `FIORA-Base-and-Motor-Mount-Build-Steps.jpg`
- Size: 750×320, JPG
- Section: Building the Base, Couplers and Motor Mounts (top of the section)
- Source: foam base (`0542a37a…`), triangular mounts (`b06277a8…`), assembled base (`7b4ed960…`), joined with black arrows and labelled STEP 1, STEP 3 and STEP 4 to match the build steps
- Alt: FIORA base build steps: circular foam-sheet base, triangular 3D-printed motor mounts, and mecanum wheels sitting in their cutouts


### 7. Coupler prints (READY, from the team's photo)
- File: `FIORA-3D-Printed-Coupler-Prints.jpg`
- Size: 420×560, JPG
- Section: Building the Base, Couplers and Motor Mounts, Step 2
- Source: Week 2 photo (`e259bcec…`)
- Alt: 3D-printed motor-to-wheel couplers for FIORA indoor delivery robot, from the more than 15 versions printed before one fitted


### 8. Controllers we tried strip (READY, from the team's photos)
- File: `FIORA-Motor-Controllers-We-Tried.jpg`
- Size: 750×450, JPG
- Section: Assembling the Drive Electronics
- Source: ESP32-S3 Pico + TB6612FNG on a breadboard (`02acdefe…`), Arduino Uno + L298 boards on the base (`d11fbb09…`), labelled FIRST TRY and SECOND TRY
- Alt: Motor controllers tried for FIORA before the L293D shield: ESP32-S3 Pico with TB6612FNG driver on a breadboard, and Arduino Uno with L298 driver boards on the base


### 9. RPLIDAR A1M8 (READY, from the team's photo)
- File: `SLAMTEC-RPLIDAR-A1M8-for-FIORA.jpg`
- Size: 750×422, JPG
- Section: Setting Up the RPLIDAR A1M8 with ROS 2 on the Raspberry Pi 5
- Source: Week 5 photo (`68d1a346…`)
- Alt: SLAMTEC RPLIDAR A1M8 360-degree LiDAR with its USB adapter board used on FIORA indoor delivery robot


### 10. Body sketch (READY, from the team's photo)
- File: `FIORA-Body-Sketch-Side-View.jpg`
- Size: 640×520, JPG
- Section: Building the FIORA Body
- Source: Week 5 photo (`6c164d37…`)
- Alt: Hand-drawn side view sketch of FIORA indoor delivery robot body with LiDAR and screen on top, two levels in the middle and a 60mm base for wheels and controllers


### 11. Prototype body with LiDAR (READY, from the team's photo)
- File: `FIORA-Prototype-Body-with-RPLIDAR-and-Raspberry-Pi-5.jpg`
- Size: 600×680, JPG
- Section: Output: Mapping TinkerSpace with FIORA
- Source: Week 7 photo (`276a3658…`)
- Alt: FIORA prototype body made of foam sheet with RPLIDAR A1M8 and Raspberry Pi 5 on the top deck and the Arduino, battery and mecanum wheels inside


### 12. RViz2 map (READY, from the team's photo)
- File: `FIORA-RViz2-Map-of-TinkerSpace.jpg`
- Size: 750×435, JPG
- Section: Output: Mapping TinkerSpace with FIORA
- Source: Week 7 photo of the laptop screen (`cdb55a54…`), cropped to the RViz2 window
- Better version: a straight screenshot of RViz2 with the Map and Laser Scan displays, or a saved map image from Week 8.
- Alt: RViz2 map of TinkerSpace built with the RPLIDAR A1M8 on FIORA indoor delivery robot, showing free space, black obstacle cells and the robot position


### Video (READY, team clip)

| # | File in `videos/` | Section | Source (weekly log, GitHub attachment) |
|---|---|---|---|
| V1 | `FIORA-LiDAR-Mapping-Run.mp4` (poster `.jpg`) | Live Video Demonstration | Week 7, `bc92c07e…` |

Note: Circuit Digest articles normally carry one YouTube embed. If the team publishes a cut on YouTube, it can replace V1 in the CMS version.

Not used: the Week 3 bracket image (`353e7949…`) is a stock product photo, and the Week 5 design-session photo (`de93ace8…`) shows people more than the design.


### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
