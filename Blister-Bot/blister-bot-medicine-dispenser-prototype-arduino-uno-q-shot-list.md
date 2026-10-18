# Shot list: Blister Bot medicine dispenser prototype article

9 images and 1 video in article order, all ready in `images/` and `videos/`. The article is a replication guide (parts, wiring, printing, assembly, setup, testing), so each image sits under the build step it illustrates:

- 5 drawn by digestdocs: hero, block diagram, flowchart, components grid and wiring diagram. All are on white; four are black line art, and the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 1 rendered from the team's own STL files (`cad/new3d.stl`, `cad/medicinewheelstand.stl`, `cad/blissupport.stl`) with a small flat-shaded renderer.
- 3 made from the team's photos in `assets/`: the CNC gantry, the medicine holder with a pack, and the SAM 2 output.
- 1 video: the team's CNC moving trial from `assets/cncmovingtrial.mp4`, transcoded to H.264 MP4 (fast start) with a poster frame. In the Markdown it is a `<video>` block that plays the local file first and falls back to the raw GitHub copy. In the PDF it shows the poster and a link.

Not used, on purpose:
- `Week 1/3D Demo Animation.mp4` (in git history): an AI-generated concept video with a generator watermark, not footage of the build. Using it in the article could make readers think it shows the real machine.
- The Week 1 Blender scoring animations (in git history): 5-second renders that are hard to read without the deleted reports around them.
- `code/facerecog-unoq/faces/*.jpg`: face crops of real people.
- `assets/arduinoboardimage.webp`: a manufacturer board image, not the team's.
- The green-background test photo in `code/blister_detector/outputs/` (`testmed2`): looks like a stock photo.

All images are 750 px wide or less, JPG, no watermark.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `Blister-Bot-Medicine-Dispenser-Prototype.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Brief for a photo version: the gantry with the medicine wheel and a blister pack loaded, on a plain desk, soft daylight. Title in heavy uppercase on two lines, "BLISTER BOT" in white and "MEDICINE DISPENSER PROTOTYPE" in a red accent, top area.
- Alt: Blister Bot Medicine Dispenser Prototype

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-Blister-Bot-Medicine-Dispenser.jpg` (source: `.svg`)
- Size: 750×540
- Section: How Does the Blister Bot Medicine Dispenser Work?
- Note: the wheel motor is dashed because it is not in the firmware yet. Drivers labelled "L293D or ULN2003" because the repo names both.
- Alt: Block diagram of Blister Bot medicine dispenser showing microphone, two USB cameras, Arduino UNO Q Linux side with AI models, STM32 side, stepper drivers and 28BYJ-48 motors

### 3. Master controller flowchart (READY, drawn)
- File: `Blister-Bot-Master-Controller-Flowchart.jpg` (source: `.svg`)
- Size: 750×1000
- Section: How Does the Blister Bot Medicine Dispenser Work?
- Note: drawn from `code/master_controller.py`, including the note that there is no face check before drilling.
- Alt: Flowchart of Blister Bot master controller showing boot, voice setup of caretakers and medicines, wake word, intent classification, drill routine and spoken answers

### 4. Components grid (READY, drawn as line icons)
- File: `Components-Required-for-Blister-Bot-Medicine-Dispenser.jpg` (source: `.svg`)
- Size: 750×480, JPG
- Section: Components Required for Blister Bot (above the table)
- Brief for a photo version: white background, cut-out photos in a 5 + 5 grid, bold uppercase labels: "ARDUINO UNO Q", "28BYJ-48 ×3", "STEPPER DRIVER ×3", "USB WEBCAM ×2", "USB MICROPHONE", "WIRED EARPHONE", "6V 4×AA PACK", "3D-PRINTED GANTRY", "MEDICINE WHEEL", "BLISTER PACK".
- Alt: Components required for Blister Bot including Arduino UNO Q, 28BYJ-48 stepper motors, stepper drivers, USB webcams, USB microphone, earphone, 4xAA pack, 3D-printed gantry, medicine wheel and blister pack

### 5. Circuit diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-Blister-Bot-Medicine-Dispenser.jpg` (source: `.svg`)
- Size: 750×590, JPG
- Section: Circuit Diagram of Blister Bot
- Title attribute: Circuit Diagram of Blister Bot Medicine Dispenser
- Connections drawn (from `docs/connections.md` and `cnc_plotter.ino`):
  - X driver IN1 to IN4 on UNO Q pins 2, 3, 4, 5; Y driver on 6, 7, 8, 9; Z driver on 10, 11, 12, 13
  - Each 28BYJ-48 into its driver
  - Driver + and − to the breadboard rails, rails fed by a 6V 4×AA pack
  - UNO Q GND to the ground rail (common ground)
- Not recorded, drawn dashed or as a note: the USB-C hub for the cameras and mic, the earphone connection, the driver type (L293D in the README, ULN2003-style in connections.md), and the wheel motor (not wired).

### 6. CNC gantry prototype (READY, from the team's photo)
- File: `Blister-Bot-3-Axis-CNC-Gantry-Prototype.jpg`
- Size: 600×750, JPG
- Section: 3D Printing the Gantry and the Medicine Wheel (gantry files)
- Source: `assets/cncprototype.jpg`, cropped. The motor labels read "28BYJ-48 5VDC".
- Alt: Blister Bot 3-axis CNC gantry prototype with three 28BYJ-48 stepper motors on 3D-printed rack and pinion rails on a cardboard base

### 7. Medicine wheel and stands CAD (READY, rendered from the team's STL files)
- File: `Blister-Bot-Medicine-Wheel-and-Stands-CAD.jpg`
- Size: 750×340, JPG
- Section: 3D Printing the Gantry and the Medicine Wheel (wheel files)
- Note: measured from the STLs: wheel 154 × 154 × 97 mm, each stand 50 × 50 × 135 mm. A render from Zoo/KCL or a slicer would look nicer.
- Alt: CAD render of Blister Bot medicine holder wheel with four blades and the two 3D-printed stands that carry it

### 8. Medicine holder with a pack (READY, from the team's photo)
- File: `Blister-Bot-Medicine-Holder-with-Blister-Pack.jpg`
- Size: 750×563, JPG
- Section: Assembling Blister Bot, Step 2 (mount the wheel and the cameras)
- Source: `assets/medholderphoto.jpg`, cropped
- Alt: Blister Bot 3D-printed medicine holder with a blue blister pack held in the blade over the open window

### 9. SAM 2 output (READY, from the team's output image)
- File: `SAM-2-Pill-Boundaries-on-Blister-Pack.jpg`
- Size: 480×640, JPG
- Section: Output: Testing the Blister Bot Prototype
- Source: `assets/sample_result.jpg`
- Alt: SAM 2 pill boundaries drawn in red around each bubble of a blue blister pack for Blister Bot

### V1. CNC gantry moving trial (READY, team clip)
- File: `videos/Blister-Bot-CNC-Gantry-Moving-Trial.mp4` with poster `.jpg`
- Section: Live Video Demonstration
- Source: `assets/cncmovingtrial.mp4` (6 seconds); fallback source `https://raw.githubusercontent.com/RealASHWIN122/Blister-bot-main-/main/assets/cncmovingtrial.mp4`
- Wanted: a clip of the full voice-to-drill sequence once the drill works, and a short clip of the voice assistant answering.

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
