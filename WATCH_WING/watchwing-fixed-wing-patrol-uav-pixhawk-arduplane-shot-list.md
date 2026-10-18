# Shot list: WatchWing fixed-wing patrol UAV article

8 images and 9 videos in article order, all ready in `images/` and `videos/`:

- 5 images drawn by digestdocs: hero, block diagram, flowchart, components grid and wiring diagram. All are on white; four are black line art, and the flowchart uses the skill's standard colour coding (as in the ARGUS article). Each has an editable `.svg` next to its `.jpg`.
- 3 images made from the team's photos, which are linked from the weekly logs as GitHub attachments: the foam strip (three photos joined), the finished airframe and the electronics bay.
- 9 videos: the team's own clips from the weekly logs, transcoded to H.264 MP4 (fast start) with a poster JPG each. In the Markdown they are `<video>` blocks that play the local file first and fall back to the GitHub-hosted original, so they still play when the .md file is sent on its own (with an internet connection). In the PDF each one shows its poster frame and a clickable link.

All images are 750 px wide or less, JPG, no watermark. If the publishing site uses a logo watermark, add it to the drawn images only.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `WatchWing-Fixed-Wing-Patrol-UAV.jpg` (source: `.svg` next to it)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Brief for a photo version: the finished Simple Scout on grass or a plain floor, top three-quarter view, soft daylight. Title in heavy uppercase on two lines, "WATCHWING" in white and "FIXED-WING PATROL UAV" in a red accent, top area, clear of the aircraft. The airframe was lost in flight 3, so a photo version needs a rebuilt aircraft; `docs` week 7 has the closest existing shot (wood-grain tape finish, no electronics).
- Alt: WatchWing Fixed-Wing Patrol UAV

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-WatchWing-Fixed-Wing-UAV.jpg` (source: `.svg`)
- Size: 750×560
- Section: How Does the WatchWing Fixed-Wing UAV Work?
- Note: The dashed box and link are the Raspberry Pi camera and its planned MAVLink link, which were bench-tested only.
- Alt: Block diagram of WatchWing fixed-wing UAV showing FS-i6 transmitter, FS-iA10B receiver, M10 GPS, Pixhawk 2.4.8, SG90 servos, SimonK ESC, A2212 motor and 3S LiPo

### 3. Flight sequence flowchart (READY, drawn)
- File: `WatchWing-Flight-Sequence-Flowchart.jpg` (source: `.svg`)
- Size: 750×1024
- Section: How Does the WatchWing Fixed-Wing UAV Work?
- Note: The bracket marks AUTO, the DO_JUMP loop and RTL as configured but not flown.
- Alt: Flowchart of WatchWing flight sequence showing boot, pre-arm checks, arming, hand launch, AUTO waypoint loop with DO_JUMP, RTL and landing

### 4. Components grid (READY, drawn as line icons; product photos can replace them later)
- File: `Components-Required-for-WatchWing-Fixed-Wing-UAV.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required for the WatchWing Fixed-Wing UAV (above the table)
- Brief for a photo version: white background, cut-out photos in a 5 + 5 grid, bold uppercase label under each: "PIXHAWK 2.4.8", "M10 GPS MODULE", "FLYSKY FS-i6", "FS-iA10B RECEIVER", "A2212 1400KV MOTOR", "SIMONK 30A ESC", "3S 3300mAh LIPO", "SG90 SERVO ×4", "PROPELLER", "5 mm DEPRON SHEET". Add the prop size to its label once known.
- Alt: Components required for WatchWing fixed-wing UAV including Pixhawk 2.4.8, M10 GPS, FlySky FS-i6, FS-iA10B receiver, A2212 motor, SimonK ESC, LiPo, SG90 servos and Depron sheet

### 5. Wiring diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-WatchWing-Fixed-Wing-UAV.jpg` (source: `.svg`)
- Size: 750×600, JPG
- Section: Wiring Diagram of the WatchWing Fixed-Wing UAV
- Title attribute: Wiring Diagram of WatchWing Fixed-Wing UAV
- Connections drawn, all stated in the repository README (Wiring section and MAIN OUT table), none assumed:
  - FS-i6 → FS-iA10B over 2.4 GHz
  - FS-iA10B PPM output (signal, 5V, GND) → Pixhawk RC IN
  - M10 GPS cable → GPS port; M10 compass (IST8310) cable → I2C port
  - Laptop → Pixhawk micro-USB
  - MAIN OUT 1 left aileron SG90, 2 elevator SG90, 3 SimonK 30A ESC (signal + BEC 5V to the rail), 4 rudder SG90, 5 right aileron SG90; 6 to 8 unused
  - 3S LiPo 3300mAh → ESC only; ESC → A2212 1400KV (3 phase wires)
- Brief for a Fritzing/Cirkit version: light grey background (#E6E6E6), realistic module drawings, red = +, black = GND, green = signal, bold label next to each module.

### 6. Foam materials strip (READY, from the team's photos)
- File: `Foam-Materials-Tried-for-WatchWing-Airframe.jpg`
- Size: 750×320, JPG
- Section: Building the WatchWing Airframe
- Source: week 3 Sunboard wing photo (`092af938…`), week 5 Thermocol photo (`8e9ed856…`), week 7 finished Scout photo (`465b7bbe…`), joined with black arrows and labels
- Alt: Foam materials tried for WatchWing airframe: heavy PVC Sunboard wing, Thermocol with a jagged hot-wire cut, and the finished 5mm Depron Simple Scout

### 7. Finished Simple Scout airframe (READY, from the team's photo)
- File: `Flite-Test-Simple-Scout-Airframe-Built-from-Depron.jpg`
- Size: 750×500, JPG
- Section: Building the WatchWing Airframe
- Source: week 7 photo (`db6aab41…`), cropped to 3:2
- Alt: Flite Test Simple Scout airframe built from 5mm Depron for WatchWing fixed-wing UAV, with wing, fuselage and tail covered in tape

### 8. Electronics bay (READY, from the team's photo)
- File: `WatchWing-Electronics-Bay-with-Pixhawk-ESC-and-Servos.jpg`
- Size: 750×500, JPG
- Section: Hardware Assembly of WatchWing
- Source: week 9 photo (`13f61bea…`), rotated 90° so the fuselage runs left to right, cropped to 3:2. The red "SimonK 30A" ESC, the FS-iA10B receiver, the side-mounted Pixhawk and two SG90s are visible.
- Alt: Electronics bay of WatchWing fixed-wing UAV with 3S LiPo, SimonK 30A ESC, side-mounted Pixhawk, FS-iA10B receiver and SG90 servos

### Videos (READY, team clips)

| # | File in `videos/` | Section | Source (weekly log, GitHub attachment) |
|---|---|---|---|
| V1 | `WatchWing-Hot-Wire-Cutting-Thermocol.mp4` | Building the WatchWing Airframe | Week 5, `4cb5d6a5…` |
| V2 | `WatchWing-Control-Surface-Check.mp4` | Hardware Assembly | Week 9, `c18ed667…` |
| V3 | `WatchWing-Radio-Calibration-in-Mission-Planner.mp4` | Mission Planner Setup, Step 3 | Week 8, `d9e56841…` |
| V4 | `WatchWing-Servo-Output-in-Mission-Planner.mp4` | Parameter Configuration, Arming and Safety | Week 8, `6a6e90e5…` |
| V5 | `WatchWing-Flight-1.mp4` | Live Video Demonstration | Week 9, `8a103069…` |
| V6 | `WatchWing-Flight-2.mp4` | Live Video Demonstration | Week 10, `e85e026e…` |
| V7 | `WatchWing-Flight-3.mp4` | Live Video Demonstration | Week 10, `d0688072…` |
| V8 | `WatchWing-Static-Thrust-Test.mp4` | Pre-Flight Checks and Testing | Week 9, `7c95ffb8…` (original is a .MOV) |
| V9 | `WatchWing-Airframe-After-Flight-3.mp4` | Flight Tests (Output) | Week 10, `42bfe03f…` |

Notes:
- The Mission Planner clips (V3, V4) are phone recordings of the laptop screen, so the screen text is soft. Straight screenshots of **Radio Calibration** and **Servo Output** would read better.
- Circuit Digest articles normally carry one YouTube embed. If the team publishes a cut of the flights on YouTube, it can replace V5 to V7 in the CMS version.

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
