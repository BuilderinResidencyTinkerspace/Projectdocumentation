# Shot list: AquaNav fish-following rover article

The article is a replication guide: media sit under the build step they illustrate, in build order.

12 images and 5 videos in article order, all ready in `images/` and `videos/`:

- 5 drawn by digestdocs: hero, block diagram, flowchart, components grid and wiring diagram. All are on white; four are black line art, and the flowchart uses the skill's standard colour coding (as in the ARGUS and WatchWing articles). Each has an editable `.svg` next to its `.jpg`.
- 7 made from the team's photos, which are linked from the weekly logs as GitHub attachments.
- 5 videos from the weekly logs, transcoded to H.264 MP4 (long side 854 px or less) with a poster `.jpg` next to each. Each `<video>` block also lists the original GitHub attachment URL as a second source, so it still plays when the Markdown is opened without the `videos/` folder.
- One Week 7 clip (`https://github.com/user-attachments/assets/dc08beaf-70f6-4dd8-a332-46d6dd5b2897`) returns 404 and could not be used.

All images are 750 px wide or less, JPG, no watermark.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `AquaNav-Fish-Following-Rover.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Note: the tracking label "CENTRE (322, 267)" is the centre value shown in the team's OpenCV clip.
- Brief for a photo version: the finished rover on the tiled floor, three-quarter front view, the red Betta visible in the tank and the camera mast in frame. Title in heavy uppercase on two lines, "AQUANAV" in white and "FISH-FOLLOWING ROVER" in a red accent, top area, clear of the mast. The Week 9 photo (`9dddd87e…`) is the closest existing shot.
- Alt: AquaNav Fish-Following Rover

### 2. Block diagram (READY, drawn)
- File: `Block-Diagram-of-AquaNav-Fish-Following-Rover.jpg` (source: `.svg`)
- Size: 750×560
- Section: How Does the AquaNav Fish-Following Rover Work?
- Note: the Raspberry Pi's own power source is left out because the repo does not show it.
- Alt: Block diagram of AquaNav fish-following rover showing the fish, Pi Camera Module 3, Raspberry Pi 5, web dashboard, NodeMCU, two L298N drivers, battery and four DC motors

### 3. Movement logic flowchart (READY, drawn)
- File: `AquaNav-Movement-Logic-Flowchart.jpg` (source: `.svg`)
- Size: 750×712
- Section: How Does the AquaNav Fish-Following Rover Work?
- Note: follows the build notes (four zones plus a centre zone, move 5 to 8 s, wait about 10 s). The tracking code itself is not in the repo.
- Alt: Flowchart of AquaNav movement logic showing frame capture, HSV fish detection, centre zone check, grid-zone movement for 5 to 8 seconds and a 10-second wait

### 4. Components grid (READY, drawn as line icons)
- File: `Components-Required-for-AquaNav-Fish-Following-Rover.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required for the AquaNav Rover (above the table)
- Brief for a photo version: white background, 5 + 5 grid, bold uppercase labels: "RASPBERRY PI 5", "CAMERA MODULE 3", "NODEMCU ESP8266", "L298N DRIVER ×2", "12V DC MOTOR ×4", "WHEEL ×4", "LI-ION CELL ×3", "ROCKER SWITCH", "GLASS AQUARIUM", "ALUMINIUM FRAME". Add the motor RPM, wheel size and final battery to the labels once known.
- Alt: Components required for AquaNav fish-following rover including Raspberry Pi 5, Camera Module 3, NodeMCU, L298N drivers, 12V DC motors, wheels, Li-ion cells, switch, glass aquarium and aluminium frame

### 5. Wiring diagram (READY, drawn black on white)
- File: `Wiring-Diagram-of-AquaNav-Fish-Following-Rover.jpg` (source: `.svg`)
- Size: 750×640, JPG
- Section: Wiring Diagram of the AquaNav Rover
- Title attribute: Wiring Diagram of AquaNav Fish-Following Rover
- Connections drawn:
  - Pi Camera Module 3 → Raspberry Pi 5 CSI ribbon (seen in the Week 7 photo)
  - Raspberry Pi 5 → NodeMCU over USB serial (Week 7 log)
  - NodeMCU → IN1 to IN4 of two L298N boards *(stated as "motor-driver connections"; the GPIO pin map is not in the repo)*
  - Each L298N → two 12V Johnson DC motors (2 drivers, 4 motors in the logs)
  - Battery → switch → both L298N 12V inputs, common GND *(assumed: standard wiring; the Week 9 log only says "a battery and a switch")*
  - NodeMCU powered over the Pi's USB *(assumed)*
- Brief for a Fritzing/Cirkit version: light grey background (#E6E6E6), realistic modules, red = +, black = GND, green = signal, real GPIO numbers once the pin map is known.

### 6. Rover bases strip (READY, from the team's photos)
- File: `Rover-Bases-Tried-for-AquaNav.jpg`
- Size: 748×320, JPG
- Section: Building the AquaNav Rover Base
- Source: Week 1 shoe rack (`6b393a8a…`), Week 1 plywood base (`f3c55afa…`), Week 4 aluminium frame rover (`dc8096ea…`)
- Alt: Rover bases tried for AquaNav: a shoe rack that was not strong enough, a plywood base, and the aluminium frame used from Week 4

### 7. Mecanum wheels and printed shafts (READY, from the team's photos)
- File: `AquaNav-Mecanum-Wheels-and-3D-Printed-Shafts.jpg`
- Size: 720×320, JPG
- Section: Building the AquaNav Rover Base
- Source: Week 2 photos (`adf1c08a…`, `29aa1b4a…`)
- Alt: 60 mm mecanum wheels and motors on the wooden base of AquaNav, with the 3D-printed motor-to-wheel shafts

### 8. Custom aquarium with the Betta (READY, from the team's photo)
- File: `AquaNav-Custom-Aquarium-with-Betta.jpg`
- Size: 480×600, JPG
- Section: Preparing the Aquarium and the Fish
- Source: Week 3 photo (`40700e41…`)
- Alt: Custom glass aquarium for AquaNav with the red Betta in its bottle, acclimatising to the water temperature

### 9. Aluminium frame with the electronics (READY, from the team's photo)
- File: `AquaNav-Aluminium-Frame-with-NodeMCU-and-L298N.jpg`
- Size: 750×563, JPG
- Section: Hardware Assembly of AquaNav
- Source: Week 4 log photo (`0ea31927…`). The motor labels read "JOHNSON DC … GRADE-A … 12V"; the cells are marked 3200mAh.
- Alt: AquaNav aluminium frame with 12V Johnson motors, NodeMCU, L298N motor driver, breadboard and Li-ion cells, and the aquarium behind it

### 10. Video: NodeMCU wheel test (READY)
- File: `videos/AquaNav-NodeMCU-Wheel-Test.mp4` + `.jpg` poster
- Section: Hardware Assembly of AquaNav
- Source: Week 6 (`a4c982b5…`), 13 s, landscape

### 11. Perfboard circuit (READY, from the team's photo)
- File: `AquaNav-Perfboard-Circuit.jpg`
- Size: 750×563, JPG
- Section: Hardware Assembly of AquaNav
- Source: Week 9 photo (`030e5b01…`)
- Alt: Soldered perfboard circuit of AquaNav fish-following rover with the motor driver connections

### 12. Video: YOLO fish tracking (READY)
- File: `videos/AquaNav-YOLO-Fish-Tracking.mp4` + poster
- Section: Setting Up the Raspberry Pi and the Fish Detector (Step 6)
- Source: Week 5 (`0fe73372…`), 33 s, portrait, no audio. Shows "AquaNav - Blue Fish Tracking" with labels such as "LEFT - BOTTOM".

### 13. Raspberry Pi control page (READY, from the team's photo)
- File: `AquaNav-Raspberry-Pi-Control-Page.jpg`
- Size: 540×633, JPG
- Section: Controlling the Motors from the Raspberry Pi
- Source: Week 7 photo (`283bbbf0…`): page at 192.168.11.207:5000, "NodeMCU: CONNECTED", Pi 5 with the camera ribbon in front of the laptop.
- Better version: a straight browser screenshot of the page, 750×350.
- Alt: AquaNav control page served by the Raspberry Pi 5 on port 5000 with forward, left, stop, right and backward buttons and NodeMCU connected

### 14. Video: OpenCV HSV fish tracking (READY)
- File: `videos/AquaNav-OpenCV-HSV-Fish-Tracking.mp4` + poster
- Section: Testing the Fish Tracking
- Source: Week 5 log (`ec2f21c9…`), 18 s. Shows "DARK BLUE FISH DETECTED", Horizontal/Vertical zone, centre (322, 267), area 1784, terminal running dark_blue_fish_tracking.py (not in the repo).

### 15. Video: final run (READY)
- File: `videos/AquaNav-Final-Run.mp4` + poster
- Section: Live Video Demonstration
- Source: Week 9 (`6563d761…`), 41 s, portrait

### 16. Video: tracking dashboard with motor control (READY)
- File: `videos/AquaNav-Tracking-Dashboard-with-Motor-Control.mp4` + poster
- Section: Live Video Demonstration
- Source: Week 8 (`f4fea29d…`), 25 s. Robot Status panel; the movement threshold value is not readable in the clip.

### 17. Finished rover (READY, from the team's photo)
- File: `AquaNav-Fish-Following-Rover-Final-Build.jpg`
- Size: 480×640, JPG
- Section: Output of the AquaNav Fish-Following Rover
- Source: Week 9 photo (`9dddd87e…`). An ultrasonic sensor hangs loose at the front, and a red switch is visible on the frame.
- Alt: Finished AquaNav fish-following rover with the glass aquarium, red Betta, aluminium frame, four wheels and the Raspberry Pi camera mast

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
