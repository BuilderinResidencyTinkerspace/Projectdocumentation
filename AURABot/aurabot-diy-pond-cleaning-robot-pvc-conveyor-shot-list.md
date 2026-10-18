# Shot list: AURABot DIY pond cleaning robot article

10 images in article order, all ready in `images/`. No videos: the repository and its history have no video files or attachment links, so the demo section keeps a YouTube `VIDEO_ID` placeholder (item 11).

- 5 drawn by digestdocs as black line art on white: hero, block diagram, conveyor side view, components grid and planned wiring diagram. Each has an editable `.svg` next to its `.jpg`.
- 5 made from the builder's photos in `docs/photos/`. The repo has six photo files, but `week-09-frame-parts-11sep.jpg` and `week-10-aluminium-frame-bearing-cutouts-19sep.jpg` are the same file (identical checksum), so there are five distinct photos.

The article was rewritten as a replication guide (pond check, parts, planned wiring, numbered build steps, safe testing), so some sections were renamed; the images are unchanged.

All images are 750 px wide or less, JPG, no watermark. If the publishing site uses a logo watermark, add it to the drawn images only.

---

### 1. Featured hero image (READY, drawn; replace with a staged photo if you prefer)
- File: `AURABot-Pond-Cleaning-Robot.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: featured image field (above the article)
- Drawn: title block on the left; side view of a PVC hull on the water line with the 30 degree mesh conveyor lifting a bottle and weed, and the unbuilt bin dashed.
- Brief for a photo version: the assembled prototype (hulls and conveyor) on the bank of the pond, soft daylight, title "AURABOT" in white over "POND CLEANING ROBOT" in a red accent, top area.
- Alt: AURABot DIY Pond Cleaning Robot

### 2. Pond photo (READY, from the builder's photo)
- File: `Stagnant-Pond-Near-Tinkerspace-Kochi.jpg`
- Size: 750×422, JPG
- Section: Before You Build: Check Your Pond
- Source: `docs/photos/pond pic.jpg`, cropped to 16:9
- Alt: Stagnant pond near Tinkerspace in Kochi with a green mat of weed on the surface and floating litter, the site AURABot was designed for

### 3. Block diagram (READY, drawn)
- File: `Block-Diagram-of-AURABot-Pond-Cleaning-Robot.jpg` (source: `.svg`)
- Size: 750×630
- Section: How Does the AURABot Pond Cleaning Robot Work?
- Note: solid boxes are built (floating platform, conveyor); dashed boxes are planned (phone, ESP32, emergency stop, battery, drivers, motors, paddles, bin).
- Alt: Block diagram of AURABot pond cleaning robot showing phone, ESP32, emergency stop, 12V battery, motor drivers, conveyor and paddle motors, conveyor, bin and PVC hulls

### 4. Conveyor side view (READY, drawn)
- File: `AURABot-Conveyor-Side-View.jpg` (source: `.svg`)
- Size: 750×440
- Section: How Does the AURABot Pond Cleaning Robot Work?
- Note: not to scale. Shows the free bottom roller just under the surface, the driven top roller, the mesh belt with the timing-belt grip strip, the aluminium rail at 30 degrees, and the planned motor, bin and paddle (dashed). All from the README's "How it is meant to work" section.
- Alt: Side view of AURABot conveyor with bottom roller under the water surface, driven top roller, mesh belt with timing-belt grip, aluminium side rail at 30 degrees, PVC hull, bin and paddle

### 5. Components grid (READY, drawn as line icons; product photos can replace them later)
- File: `Components-Required-for-AURABot-Pond-Cleaning-Robot.jpg` (source: `.svg`)
- Size: 750×500, JPG
- Section: Components Required for AURABot (above the table)
- Top row (built): 110 mm PVC pipe + end caps ×2, aluminium channel ×2, ball bearing ×4, plastic mesh net, timing belt. Bottom row tagged PLANNED: Orange 12V geared motor, ESP32 DevKit V1, BTS7960 or L298N driver, 12V battery, emergency stop button.
- Alt: Components required for AURABot pond cleaning robot including 110 mm PVC pipe, aluminium channel, ball bearings, mesh net, timing belt and the planned motor, ESP32, driver, battery and emergency stop

### 6. Planned wiring diagram (READY, drawn black on white; nothing here is wired yet)
- File: `Planned-Wiring-Diagram-of-AURABot-Pond-Cleaning-Robot.jpg` (source: `.svg`)
- Size: 750×560, JPG
- Section: Planned Wiring Diagram of AURABot
- Title attribute: Planned Wiring Diagram of AURABot Pond Cleaning Robot
- From the repo: 12V battery (LiPo or SLA, not decided), fuse, power switch, buck converter, ESP32 DevKit V1, 2 to 3 BTS7960 or L298N drivers, Orange 12V motors for the conveyor and both paddles, emergency stop read by the ESP32 as an input.
- Assumed (marked on the diagram and in the text): fuse before switch, the buck converter feeding the ESP32's VIN, two driver boards (one for the conveyor, one for both paddles). Pin numbers are not decided.
- Redraw with real modules and GPIO numbers once the electronics are fitted.

### 7. Hull pipes, rails and mesh laid out (READY, from the builder's photo)
- File: `AURABot-PVC-Hulls-and-Aluminium-Rails.jpg`
- Size: 600×600, JPG
- Section: Building the Hulls and the Conveyor (above Step 1)
- Source: `docs/photos/week-09-frame-parts-11sep.jpg` (same file as `week-10-aluminium-frame-bearing-cutouts-19sep.jpg`)
- Alt: AURABot parts laid out before assembly, with two PVC hull pipes and end caps, aluminium banner-stand rails, a cross bar and the blue mesh net

### 8. Roller end and bearing (READY, from the builder's photo)
- File: `AURABot-Roller-End-Cap-and-Ball-Bearing.jpg`
- Size: 450×600, JPG
- Section: Building the Hulls and the Conveyor (Steps 3 and 4)
- Source: `docs/photos/week-10-bearing-closeup-19sep.jpg`. The bearing's size marking is not readable in the photo.
- Alt: AURABot PVC roller end cap with a short pipe passing through it into a ball bearing

### 9. Roller with bearings (READY, from the builder's photo)
- File: `AURABot-PVC-Roller-with-Bearings.jpg`
- Size: 450×600, JPG
- Section: Building the Hulls and the Conveyor (Steps 3 and 4)
- Source: `docs/photos/week-10-roller-with-bearings-19sep.jpg`
- Alt: AURABot PVC conveyor roller about 40 cm wide with a ball bearing fitted on each end

### 10. Assembled prototype (READY, from the builder's photo)
- File: `AURABot-Assembled-Hulls-and-Conveyor.jpg`
- Size: 750×435, JPG
- Section: Output: AURABot at Demo Day
- Source: `docs/photos/prototype-assembled-02oct.jpg`, cropped and brightened slightly (the original is dark)
- Alt: Assembled AURABot pond cleaning robot prototype with two capped 110 mm PVC hulls, PVC cross pipes and the blue mesh conveyor between aluminium side rails

### 11. Demo video (TO MAKE)
- Section: Live Video Demonstration (YouTube embed with `VIDEO_ID`)
- Suggested: a short clip of the prototype with the conveyor turned by hand to show the belt moving over the rollers. If a clip from the demo on 20 September 2026 exists, use that. When available, it can also go in the Markdown as a `<video>` block like the other BIR write-ups.

### GitHub buttons
- Site assets ("Code & Schematics" and "Download Zip"); links already filled.
