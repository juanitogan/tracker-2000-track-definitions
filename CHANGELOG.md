# Tracker 2000 parts file changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This project DOES NOT ENTIRELY adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
Instead, it uses the release year as the first part of the version number.

### Rules for when to add a new part

Purely cosmetic changes (such as differences in paint or color/design of power base) does not warrant a new part.  This is not a wiki of historic part variations.  Exception: If the manufacturer designates a new part number for something, then it _should_ also be included as a new part here.

For example, the Ninco 10114 Starting Grid is identical to the 10103 Half Straight, except that it also has starting grid paint (which one could fairly argue provides a functional difference).  Thus, because the Starting Grid has its own part number, it is added here as a separate piece.  Yet, on the other hand, there are two different versions of the 10114 Starting Grid -- the older one has thinner paint lines and less staggered grid marks -- the newer one was introduced circa Ninco's N-Digital line.  These two versions should not be entered as separate parts.

My personal preference is to update the paint to the latest version, unless it is either a rare version, or is only a minor change that might look worse on screen.  For example, Ninco changed their Lane Changer paint from separated-red-white silkscreening to red-on-top-of-white silkscreening.  In this app, the older way looks better on screen -- especially when you alternate the draw order of the red/white striping (see the Ninco 10111 Crossover \[that I have yet to update\] for how muddy it can look when you do not alternate the red and white Z order).

### Drawing hints

Not in the T2K help file: Setting the Lane Distance to 0 hides the built-in lane lines completely so that you can draw your own (for crossovers, chicanes, whatever).

If drawing a Freeform part, consider first defining that part as a similar Straight or Curve and then using that auto-produced image as a template to draw the freeform part on top of.  Then, when done drawing on top of the template part, change the type to Freeform.  The editor keeps all your drawn items in place when switching part types.

Similarly, when drawing custom lanes on the ordinary types, set the Lane Distance however you need to use those lane lines as a template before setting the Lane Distance to 0 to hide the auto-drawn lane lines.


<!-- ## [Unreleased] -->


## [2026.1] - 02JAN2026 MJJ

Text editor find/replace chart for repairing breaking changes in TR3 files:

| Old           | New              |
|---------------|------------------|
|```10109```    |```10101-OR``` - this is the off-road powerbase - it merely marks the spot where you need to manually replace it with 10103,10102,10103 in T2K |
|```10117```    |```10117-L```\*   |
|```10117-L1``` |```10117-R```\*   |
|```10117-L2``` |```10117-L```     |
|```40204-223```|```40204-R2L```   |
|```40204-322```|```40204-L2R```   |
|```10504-SE``` |```10504-SE-L```\*|
|```10504-M```  |```10504-M-L```\* |

\* Best guess of L/R considering past usage (not lane color).  Check and fix in T2K after text editing.

### Breaking changes
- I keep breaking my own updates only because this doesn't affect my tracks greatly and because my additions have yet to be in use by anyone outside our club.  I think I've worked out the proper standards for these odd pieces now.
- Removed 10117 Single-lane Straight and also renamed 10117-L1 and -L2 to 10117-R and -L (for better consistancy with other Ninco pieces, as well as the Policar set I'm working on).
- Renamed the 40204 Multilane LCs from 40204-223 and -322 to 40204-R2L and -L2R... both for consistancy with the 40201 yLCs and because lane numbering can be confusing since it depends on direction as to whether lane 1 is on the left or the right (but usually being the inside lane either way).

### Changes
- I just learned there is a hard limit of 32 track definitions.  Thus, deleting the suspiciously sparse SCX-DIGITAL kit (in favor of SCXDIGITAL2) to make room for Policar.
  - Also moving BITCHARG, ROUTED and ROUTEDMETRIC to their own file (and then think about dividing by scale instead) to make room for Policar + Ninco and Policar + Fleischmann.
  - Also changing order of kits in the file a bit (more alphabetical, by plastic, then by custom/routed/wood).
- Updated the SCX-NINCO kit to bring in latest Ninco changes (SCX side not updated) and renamed it to "Ninco + SCX / Scalextric" to match my own standard of adapter supplier first and on top.
- Finally (!) learned that you can hide the slot lines by setting Lane Distance to 0 (it's not in the help file).  Thus, cleaned up the art on the Ninco chicanes, corner crossovers, single lanes, and adapters.
  - Note: SCX lane-spacing dimensions in inches: 0, 1.53125, 4.59375, 6.125; in cm: 0, 3.889375, 11.66812, 15.5575.
  - (18 - 15.5575) / 2 = 1.22125 cm offset; 3.889375 + 1.22125 = 5.110625; 4.5 - 1.22125 = 3.27875
  - Thus, 10110-N2S lane points: 4.5,0 | 13.5,0 | 5.110625,20 | 12.889375,20
  - Thus, 10110-S2N lane points: 3.889375,0 | 11.66812,0 | 3.27875,20 | 12.27875,20
- Minor Ninco part name changes.
- Replaced the Ninco 10504 roundabout pieces with Freeform pieces instead of Curve pieces.  Thus, inventory will be less automated, but they will now make more sense as to what fits where and which way it turns.  (Better art too since T2K can't draw curves at unusual angles well; see v2024.1 below.)
  - 10504-SE **Left** Lane node coordinates based on 47.4 deg and 31.9cm outer radius (9.0 offset + 31.9 = 40.9) even though setting angle at 47.25 in T2K:
    - Outer arc: 9,0 | 40.9-21.59234= 19.30766,23.4815
    - Inner arc: 18,0 | 40.9-15.50046= 25.39954,16.85662
    - Lane arc: 13.5,0 | 40.9-18.5464= 22.3536,20.16906
	- Next x,y: 40.9-27.68423= 13.21577,30.10637
	- Then copy Left Lane and mirror the silk screen (Ctrl+M) to create Right Lane:
	- Next x,y: -22.9+15.50046= -7.39954,16.85662
  - 10504-M **Right** Lane node coordinates based on 45.8 deg and 23.8cm outer radius (9.0 offset + 23.8 = 32.8) even though setting angle at 45.75 in T2K:
    - Outer arc: 0,0 | 23.8-16.59253= 7.20747,17.06247
    - Inner arc: 9,0 | 23.8-10.31804= 13.48196,10.61028
    - Lane arc: 4.5,0 | 23.8-13.45529= 10.34471,13.83637
	- Next x,y: 7.20747,17.06247
	- Then copy Right Lane and mirror the silk screen (Ctrl+M) to create Left Lane:
	- Next x,y: -5.8+4.04356= -1.75644,4.15808
- Scalextric Super 124 changes:
  - Changed name from "Super 1:24" (I didn't know what this was) to "Scalextric Super 124" (after some creative searching \[for `12" 1:24 slot car track pieces uk`\] I found it).
  - Changed the length of the straight from 10.75" to 10.69" to match the spec from the catalog (which, yes, is an oddly specific length, and I can only guess it has something to do with figure 8s... but none of the figure 8s are near perfect).
  - Changed the lane width from 6" to 8" (it is really 3 lanes with 4" between each).
  - Changed the border width from 8cm to 2" (best guess based on photos).
  - Missing parts from track def (based on 1968-1970 catalogs) due to unknown dimensions:
	- 24T/8 Banked Curve
	- 24T/9 Banking Approach (24T/9-S\[tart\] and 24T/9-E\[nd\])

### Additions
- Added Policar (2017) to the set of track defs.  Notes:
  - I did not use the Interface part type for the Ninco and Fleischmann adapter parts because interfaces do not allow borders (stupidly) and, with Policar only 1mm more narrow, I doubt they tapered their adapters at all.  And, yes, Policar's adapters do allow their usual borders.  On the other hand, only Interface and Freeform parts allow an offset, so we lose the 0.5mm offset by using a Straight type part here.  Correct offset or allow borders???  Which is more important?  Going with borders since this is a very minor offset that is lost (it takes 10x zoom to see it).
  - After much back and forth, I decided to handle the single-lane pieces (just like my Ninco edits) by: (1) two part entries for left and right lanes, and (2) a Freeform part type for the left lane (no borders allowed) and a narrow Straight part for the right lane (to allow for border(s) at least on the right lane).  Previously, with Ninco, I used a Straight part type for the left lane as well--with the right half of it whited and X'd out--but I've since moved on from that, favoring a cleaner design view over the ability to add a border (since this software doesn't do border super well anyhow--meaning any borders I add in this software prove to be just an approximation regardless).
  - I made the single-lane pieces 8.9cm wide instead of 8.95cm because, by my math, this is what they would have had to do to keep them bi-directional on 9cm slot centers (and, thus, guessing a 1mm gap between them).  Someone can correct this if I'm wrong (or if Policar isn't really 9cm but 8.95cm between slots and they fudge it).  UPDATE: I finally found an image that states "90mm (89.5 nominal)."  So, correcting things now to 8.95cm.
- Added Policar + Ninco as a merged kit.
- Added Policar + Fleischmann as a merged kit (did not update Fleischmann).
- Added Scalextric Super 124 "Fly-over Bridge" (24T/7) parts: 24T/7-B\[ase\] and 24T/7-S\[ummit\] (conveX and concaVe).  Currently, they are set to the same length and travel as a straight but at least one of those two values should be different by a millimeter or so; we just don't know which until someone measures them.


## [2025.2] - 27NOV2025 MJJ

### Changes
- Corrected the 10110 Ninco-SCX adapter "chicane" from 22.3cm to 20.0cm and 20.0093cm travel (based on 3-1/16" SCX lane spacing, 7.77875cm).  (Not the first crazy dimension I've seen like this.)  Also corrected Width 1 from 15.5572 to 15.5575 (6-1/8").


## [2025.1] - 11SEP2025 MJJ

### Changes
- Added hash marks to all pieces with N-Digital sensor strips to mark where the sensor strips are.  This is to help avoid placing pieces backwards when assembling the track from a b/w outline printout.  Also moved the lane-change lines on 40208 slightly to accommodate the sensor marks (and they are now more accurate for it).


## [2024.1] - 06MAR2024, 01APR2024, 03JUL2024 MJJ

### Breaking changes (removals)

Text editor find/replace chart for repairing breaking changes in TR3 files:

| Old           | New            |
|---------------|----------------|
|```10109```    |```10101-OR``` - this is the off-road powerbase - it merely marks the spot where you need to manually replace it with 10103,10102,10103 in T2K |
|```40202-G```  |```10114```     |

- Removed "Bridge Complete" because 10109 is a kit consisting of other track pieces (1x 10102, 2x 10103, etc.) just like any other Ninco kit.  Whoever first added this did the world a disservice.  Now, 10506, the Dune Extension Kit (an off-road bridge) needs some special attention at some point.  Even that, however, looks like it is made up of 2x of this and 2x of that.  Which, of course, should be entered separately so that bridges can be extended however on chooses.
- Removed 40202-G (a made-up part number) in favor of the 10114 starting grid, but updated the paint on 10114 to the latest version.  This fixes my mistake about the N-Digital-era starting grid being a different part number than the older starting grid with different paint.  Only the paint differs, not the part number.
- Removed 40204-223L, 40204-223R, 40204-322L, and 40204-322R (all made-up numbers I added earlier) in favor of doing it different.  I now handle the 40204 multilane changers with 40204-223, 40204-322, and 10117-L1 (which, yes, are still made-up part numbers).  Splitting these parts into 3+1 lanes, instead of 2+2 lanes, is both more obvious and allows me to show three lanes on a 2-lane drawing.  The stock you enter for 10117-L1 should be equal to the stock for 40204-223 plus 40204-322.

### Changes
- Updated the art on 10101 Starting Straight and 10111 Crossover.
- Removed the inner border from 10101 Starting Straight due to power hub.
- Thought 40204-223 and 40204-322 were named backwards... fixed... then reverted... when I remembered lane 1 is furthest from the powerbase.

- Fixed roundabout pieces... as close as Tracker 2000 will let me.  Note that the angle field rounds to the nearest 0.25 degrees (and doesn't draw them right unless they are even halves of 90 degrees).  This rounding could likely be overridden by manually editing the Tracker30.df3 file in a text editor, but that would just make it difficult for later users trying to tweak things.  (Side note about angles: For the middle pieces, find the angle, then note the difference between that angle and 45 degrees.  The angle of the start/end pieces should be 45 plus that difference times 3, or: `(m - 45) * 3 + 45 = s`.)
  - Proper angles and values (according to my own measurements):

  | Part             | Angle | Outer Radius | Inner Dist. | Outer Dist. | notes |
  |------------------|------:|--------:|--------:|--------:|-------|
  | 10504-SE old     | 45.00 | 36.5370 | 29.5596 | 29.5604 |
  | 10504-SE new     | 47.40 | 31.9000 | 22.6676 | 22.6676 | close to inner R2 but not same |
  | 10504-SE rounded | 47.25 | 31.9000 | 22.6676 | 22.6676 | close to inner R2 but not same |
  |**10105 inner R2**| 45.00 | 33.1370 | 22.4914 | 22.4914 | **for comparison**; inner border steps: 14 |
  | 10504-M  old     | 45.00 | 24.1370 | 17.2391 | 17.2399 |
  | 10504-M  new     | 45.80 | 23.8000 | 15.4277 | 15.4277 | close to outer R1 but not same |
  | 10504-M  rounded | 45.75 | 23.8000 | 15.4277 | 15.4277 | close to outer R1 but not same |
  |**10106 outer R1**| 45.00 | 24.1370 | 15.4229 | 15.4229 | **for comparison**; outer border steps: 18 |

  - Note that the roundabout doesn't return to the other lane precisely.  It comes back a little narrow.\
    This is true with the actual kit as well.  It's about 5-6mm too narrow.
  - Note that I added "(right only)" to the 10504-SE description and "(left only)" to the 10504-M description.  This is true when these are added to the red lane (the default), but please note that the opposite is true when using these in the green lane.

- Changed the color of the lane in the pit-lane pieces from red to green (to make it more clear what is what when designing creative pit lanes).

### Additions
- Added 10115 R5 outer curve.
- Added 10116 1/8 straight.
- Added 10117 single-lane straight.  (Wish I could add this a curve to place on left or right lane.  Could not find a way to make a straight curve.)
- Added 10117-H single-lane half straight (an imaginary piece to bring balance to the force).
- Added 10506 Dune (off-road, 2 piece types).
- Added 10507 Snow Curve (3 piece types pluse l/r for each).
- Added 10508 Change Over Curve.
- Added 10509 Chicane (3 piece types pluse l/r for each).
- Added 40208 R2 double lane changer.
- Added 10401 Independant Power per Lane
- Added 10101-OR Off-road Power Base
  - Found in 20126 Master Track RAID and 20158 Pro Series Sets Off Road.
  - Perhaps there is a snow one as well.
    - Can't find a snow Master Track set and all snow track pictures so far show a PB of: tarmac, off-road, or can't tell.
    - Also, beware of things like off-road pieces painted white by user.
    - Note that snow just didn't get the same treatment as off-road, such as no snow/tarmac transition pieces.
- Added 10413 WI-CO Power Base


## [2008.1] - 29JUN2008 MJJ
- Added all currently known N-Digital track pieces.
- Added all off-road and snow track... with color!
- Smoothed the crossover lines a tad.
- Not sure when: Updated the finish-line art on 10101 Starting Straight.


## [3.0b] - 05NOV2005 Original
- The original `Tracker20.df3` found in Tracker 2000 V3.0b.


## 2.1 - 08JUN2004
- `Tracker21.df3` and earlier versions are not included in this repo.


## Other

Hint: To make red/white striping display the best on screen (if you care), alternate the order you draw/create the red and white polys (or post-edit the file in a text editor to do the alternating).  That way, it alternates which outline draws on top, giving better balance between the two.  I should maybe go back and do this for the Ninco 10111 Crossover like it did the others (removing the background, adding white polys between the reds, and alternating from the middle out).

I wonder if I have all the lanes backwards....?


[unreleased]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v2026.1...HEAD
[2026.1]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v2025.2...v2026.1
[2025.2]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v2025.1...v2025.2
[2025.1]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v2024.1...v2025.1
[2024.1]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v2008.1...v2024.1
[2008.1]: https://github.com/juanitogan/tracker-2000-track-definitions/compare/v3.0b...v2008.1
[3.0b]: https://github.com/juanitogan/tracker-2000-track-definitions/releases/tag/v3.0b
