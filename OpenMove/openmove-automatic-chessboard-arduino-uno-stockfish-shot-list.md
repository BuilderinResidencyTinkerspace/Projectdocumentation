# Shot list: OpenMove automatic chessboard article

The article is a replication guide: media sit under the build step they illustrate, in build order.

10 images in article order, all ready in `images/`. There are no videos: the repo, its weekly logs and its git history have no clips or YouTube links, so the demo section keeps a `VIDEO_ID` placeholder (item 11).

- 6 drawn by digestdocs: hero, block diagram, flowchart, components grid, wiring diagram and the board coordinate mapping. All are on white; five are black line art, and the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 3 made from the builder's images, which are GitHub attachments in the weekly logs.
- 1 rendered from the repo's own code: the PySide6 desktop GUI, run offscreen on our machine and not connected to any hardware.

The two Week 4 Azure screenshots were left out. One is a loading screen and the other shows the account email.

All images are 750 px wide or less, no watermark.

---

### 1. Featured hero image (READY, drawn; replace with a photo once the board is built)
- File: `OpenMove-Automatic-Chessboard-Prototype.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field
- Brief for a photo version: the board with the carriage visible underneath (or the board lifted to show it), a few pieces in place, soft daylight. "OPENMOVE" in white and "AUTOMATIC CHESSBOARD" in a red accent, top area.
- Alt: OpenMove Automatic Chessboard Prototype

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-OpenMove-Automatic-Chessboard.jpg` (source: `.svg`)
- Size: 750×530
- Section: How Does the OpenMove Automatic Chessboard Work?
- Note: Dashed boxes are the Stockfish API (deployed on an Azure VM, not linked to the board) and the planned Hall-effect grid.
- Alt: Block diagram of OpenMove automatic chessboard showing host computer, Arduino Uno with CNC Shield V3, DRV8825 drivers, NEMA 17 motors, XY carriage, MG90S magnet lift and Stockfish API

### 3. Firmware flowchart (READY, drawn)
- File: `OpenMove-Firmware-Command-Flowchart.jpg` (source: `.svg`)
- Size: 750×1080
- Section: How Does the OpenMove Automatic Chessboard Work?
- Note: Follows `processCommand()`, `executeChessMove()` and `mechanicallyMovePiece()` in firmware 2.7.
- Alt: Flowchart of OpenMove firmware showing safe startup, serial commands, emergency stop, HOME and GOTO handling, chess move checks, piece carrying and board trust

### 4. Components grid (READY, drawn as line icons)
- File: `Components-Required-for-OpenMove-Automatic-Chessboard.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required (above the table)
- Brief for a photo version: white background, 5 + 5 grid, bold uppercase labels: "ARDUINO UNO", "CNC SHIELD V3", "DRV8825 ×2", "NEMA 17 ×2", "GT2 BELT, 20T", "4 mm ROD ×2", "MG90S SERVO", "MAGNET", "12V 3A ADAPTER", "PRINTED RACK AND PINION". Add the magnet size once known.
- Alt: Components used for OpenMove automatic chessboard including Arduino Uno, CNC Shield V3, DRV8825 drivers, NEMA 17 motors, GT2 belt, steel rods, MG90S servo, magnet and 12V adapter

### 5. Wiring diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-OpenMove-Automatic-Chessboard.jpg` (source: `.svg`)
- Size: 750×560, JPG
- Section: Wiring Diagram of the OpenMove Chessboard
- Title attribute: Wiring Diagram of OpenMove Automatic Chessboard
- Connections drawn, from `code/hardware_smoke_test/README.md`, the Week 2 log and the firmware pin constants:
  - Motor A driver in the X socket: STEP D2, DIR D5. Motor B driver in the Y socket: STEP D3, DIR D6.
  - Shared active-low ENABLE on D8.
  - MG90S signal on the Z+ limit-switch header (D11), powered from a separate regulated 5V supply with common ground.
  - 12V 3A adapter for the motor side.
  - USB to the laptop, /dev/ttyUSB0 at 115200 baud.
- Assumed (standard, not stated): the 12V adapter enters through the shield's screw power terminal. Not recorded: what the regulated 5V supply is.

### 6. Arduino Uno and CNC Shield V3 (READY, two builder photos)
- File: `Arduino-Uno-and-CNC-Shield-V3-for-OpenMove.jpg`
- Size: 750×264, JPG
- Section: Testing the Motion Electronics on the Bench
- Source: Week 1 log attachments `e5aebdc2…` (Adiy Uno with CP2102 USB chip) and `e9a06f79…` (CNC Shield V3 with two DRV8825 drivers)
- Alt: Arduino Uno with CP2102 USB and CNC Shield V3 with two DRV8825 stepper drivers used for OpenMove

### 7. MG90S servo (READY, builder photo)
- File: `MG90S-Servo-for-OpenMove-Magnet-Lift.jpg`
- Size: 470×327, JPG (native resolution)
- Section: Testing the Motion Electronics on the Bench
- Source: Week 2 log attachment `44b3dea2…`
- Alt: MG90S servo used for the OpenMove magnet lift during the hardware smoke test

### 8. Linear servo magnet lift (READY, two Week 3 images)
- File: `OpenMove-Linear-Servo-Magnet-Lift.jpg`
- Size: 750×239, JPG
- Section: Building the Magnet Lift
- Source: Week 3 log attachments `ea00feb4…` (servo driving a printed rack) and `8d20ef53…` (3D model of the bracket, pinion and rack). Both are screenshots, and the mouse cursor in each was patched with neighbouring background pixels.
- Note: The servo in the left image is a blue 9g micro servo of the SG90 type, while the firmware comment and README specify an MG90S. The log does not say whether that image is the builder's own print or a reference picture, so the article does not claim either.
- Better version: a photo of the printed mechanism with the MG90S and magnet fitted, at both servo endpoints (1000 µs and 2100 µs).
- Alt: Linear servo magnet lift for OpenMove with a micro servo driving a 3D-printed rack, and the 3D model of the bracket, pinion and rack

### 9. Desktop GUI (READY, rendered from the repo's code)
- File: `OpenMove-Desktop-GUI.png`
- Size: 750×507, PNG
- Section: Uploading the Firmware and Running the Desktop GUI, Step 2
- Source: `code/openmove_gui.py` from commit b4f7609, rendered with PySide6 6.12 under `QT_QPA_PLATFORM=offscreen` at 1100×744, disconnected state.
- Better version: a screenshot from the builder's laptop while connected to the controller, with Origin and Board both set.
- Alt: OpenMove desktop GUI built with PySide6 showing the chessboard, connection panel, PGN box and Set Home, Reset Board, Servo and Abort buttons

### 10. Board coordinate mapping (READY, drawn)
- File: `OpenMove-Board-Coordinate-Mapping.jpg` (source: `.svg`)
- Size: 750×440
- Section: Calibrating the Board Mapping
- Note: From the Week 8 log and firmware 2.5 onwards. a1 = (0, 0), 44 mm pitch, h8 = (308, 308), plus the h1 and h8 guesses that came before it.
- Alt: OpenMove board coordinate mapping with a1 at the origin, 44 mm square pitch, h8 at 308 mm and the two wrong origin guesses

### 11. Demo video (TO MAKE)
- Section: Live Video Demonstration (YouTube embed with `VIDEO_ID`)
- Suggested content: the carriage homed at a1, 1 mm and 10 mm jogs in both axes, a GOTO to a few squares, the servo moving between 1000 µs and 2100 µs, and the GUI connected to the controller.

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
