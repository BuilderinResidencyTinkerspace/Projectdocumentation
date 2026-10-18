# Shot list: MARS modular rover article

14 images in article order, all ready in `images/`, plus the demo video still to make (item 15):

- 5 drawn by digestdocs: hero, block diagram, control flowchart, components grid and wiring diagram. Four are black line art on white; the flowchart uses the skill's standard colour coding. Each has an editable `.svg` next to its `.jpg`.
- 1 rendered from the repository's own STL files (`cad/`): the decks and probe-lift parts, with dimensions read from the files.
- 8 made from the builder's photos, which are linked from the weekly logs as GitHub attachments (several joined into two-panel strips).

There are no videos in the repository or in the weekly logs, so nothing is embedded. All images are 750 px wide or less, JPG, no watermark.

Left out on purpose: the Week 0 concept poster and render (illustrations, not the build), the Week 2 PCBCupid documentation screenshot, the Week 5 HC-05 product photo and the phone's Bluetooth pairing list (it shows the owner's personal devices and their addresses), and the Week 7 stock tyre image.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `MARS-Modular-Autonomous-Rover-System.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field
- Brief for a photo version: the Week 10 rover (`fc52876f…`) on a plain surface with both modules fitted, front three-quarter view. Title "MARS" in white over "MODULAR ROVER" in a red accent, top left.
- Alt: MARS Modular Autonomous Rover System


### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-MARS-Modular-Rover.jpg` (source: `.svg`)
- Size: 750×610
- Section: How Does the MARS Modular Rover Work?
- Note: the modules are drawn without a link to the base because the logs describe none.
- Alt: Block diagram of MARS modular rover showing phone app, HC-05, Arduino Uno, L298N, BO motors, HC-SR04 sensors, Raspberry Pi 5 camera module and Arduino Nano environmental module


### 3. Control flowchart (READY, drawn)
- File: `MARS-Base-Rover-Control-Flowchart.jpg` (source: `.svg`)
- Size: 750×680
- Section: How Does the MARS Modular Rover Work?
- Note: drawn from the behaviour in the Week 3, 5 and 6 logs, as the firmware is not in the repository. Redraw from the code once it is published.
- Alt: Flowchart of MARS base rover control loop showing ultrasonic distance check, stop and wait on obstacle, and Bluetooth drive commands


### 4. Components grid (READY, drawn as line icons)
- File: `Components-Required-for-MARS-Modular-Rover.jpg` (source: `.svg`)
- Size: 750×600, JPG
- Section: Components Required for the MARS Modular Rover (above the table)
- Brief for a photo version: white background, 5 × 3 grid of cut-out product photos with bold labels as in the drawing. Add the MQ model and motor rating to the labels once known.
- Alt: Components required for MARS modular rover including Arduino Uno, L298N, HC-05, HC-SR04 sensors, BO motors, 14.8V Li-ion pack, Raspberry Pi 5, webcam, Arduino Nano, gas sensor, DHT11, soil probe and servo


### 5. Battery and Arduino Uno (READY, two panels)
- File: `MARS-14-8V-Battery-and-Arduino-Uno.jpg`
- Size: 750×378
- Section: Components Required for the MARS Modular Rover (below the table)
- Source: Week 5 (`d66237ea…`, `e156726e…`)
- Alt: 14.8V 2200mAh Li-ion battery pack and the Arduino Uno that replaced the damaged ESP32-S3 in the MARS rover


### 6. Wiring diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-MARS-Base-Rover.jpg` (source: `.svg`)
- Size: 750×600, JPG
- Section: Wiring Diagram of the MARS Base Rover
- Title attribute: Wiring Diagram of MARS Base Rover
- From the logs: 14.8V pack to the L298N motor supply and to the buck converter (Week 0 power plan, Week 8), all parts on one perfboard (Week 8), three HC-SR04s at the front at centre and about ±25° (Week 6).
- Assumed (dashed, confirm on the board): buck output pin and voltage to the Uno, HC-05 TX/RX pins, HC-SR04 TRIG/ECHO pins, Uno to L298N IN1 to IN4 pins, and the motor pairs on OUT1/OUT2 and OUT3/OUT4.


### 7. 3D-printed parts (READY, rendered from the repository STL files)
- File: `MARS-3D-Printed-Decks-and-Probe-Lift-Parts.jpg`
- Size: 750×560
- Section: 3D Printing the MARS Chassis and Probe Lift
- Source: `cad/LOWERDECK_RIZ.stl`, `cad/UPPERDECK_RIZ.stl`, `cad/RizA1S.STL`, `cad/RizA2S.STL`, `cad/RizA3S.STL`. Dimensions are the files' bounding boxes. The roles of the three small parts are read from their shapes; the repository does not name them.
- Alt: 3D-printed parts of the MARS modular rover: lower deck with standoffs, perforated upper deck module plate and the three parts of the soil probe lift


### 8. First foam-board layout (READY, builder's photo)
- File: `MARS-First-Layout-on-30-cm-Foam-Board.jpg`
- Size: 600×600
- Section: Assembling the MARS Base Rover, Step 1
- Source: Week 1 log (`3b9a8554…`)
- Alt: First layout of MARS modular rover on a 30 cm foam board with four BO motors, ESP32-S3, L298N drivers, buck converter, battery cells and HC-SR04 sensors


### 9. Perfboard and integrated base (READY, two panels)
- File: `MARS-Perfboard-and-Integrated-Base.jpg`
- Size: 750×468
- Section: Assembling the MARS Base Rover, Step 4
- Source: Week 7 (`d4059c5a…`) and Week 8 (`4f78a7c2…`), labelled STEP 3 and STEP 4 to match the assembly steps
- Alt: MARS perfboard with L298N, buck converter and Arduino Uno, and the integrated base rover on the 3D-printed lower deck


### 10. Camera module (READY, two panels)
- File: `MARS-Raspberry-Pi-5-Camera-Module.jpg`
- Size: 750×468
- Section: Building the Application Modules
- Source: Week 9 (`efe43574…`, `50ae639f…`). The phone status bar and address bar were cropped out of the screenshot.
- Alt: Raspberry Pi 5 with USB webcam for the MARS camera module and the MARS ROVER live camera page on a phone


### 11. Environmental module (READY, two panels)
- File: `MARS-Environmental-Monitoring-Module.jpg`
- Size: 750×488
- Section: Building the Application Modules
- Source: Week 9 (`9d649021…`, `cc0f03f0…`)
- Alt: MARS environmental monitoring module with MQ gas sensor, DHT11 sensor and soil moisture probe on a 3D-printed servo lift


### 12. Ultrasonic room testing (READY, builder's photo)
- File: `MARS-Ultrasonic-Room-Testing.jpg`
- Size: 750×380
- Section: Testing and Calibrating the MARS Modular Rover
- Source: Week 8 (`0235e1c4…`)
- Alt: MARS modular rover on the bench during ultrasonic sensor testing with the perfboard, L298N and Li-ion pack


### 13. ESP32-S3 control page and room map (READY, two panels)
- File: `MARS-ESP32-S3-Control-Page-and-Room-Map.jpg`
- Size: 750×568
- Section: Testing and Calibrating the MARS Modular Rover
- Source: Week 3 (`2e58cbd0…`) and Week 4 (`608b7893…`), labelled FIRST CONTROLLER and ROOM MAP. The arrow characters on the control page are garbled in the original screenshot.
- Alt: MARS ESP32-S3 Wi-Fi control page with direction buttons and the hand-drawn room map with points A to K used for point-to-point tests


### 14. Final rover with both modules (READY, two panels)
- File: `MARS-Rover-with-Both-Modules.jpg`
- Size: 750×488
- Section: Testing and Calibrating the MARS Modular Rover
- Source: Week 10 (`fc52876f…`, `9671a98c…`)
- Alt: MARS modular rover with both modules fitted: webcam on the upper deck, three HC-SR04 sensors at the front and the soil probe lowered on its lift


### 15. Demo video (TO MAKE)
- Section: Live Video Demonstration (YouTube embed with `VIDEO_ID`)
- Suggested content: Bluetooth driving, stopping for an obstacle in front, an A-to-B run on the room map, the live camera page on a phone, and the servo lowering the soil probe.


### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
