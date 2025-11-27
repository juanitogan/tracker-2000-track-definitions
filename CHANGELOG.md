# Tracker 2000 parts file changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
This project DOES NOT ENTIRELY adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
Instead, it uses the release year as the first part of the version number.

### Rules for when to add a new part

Purely cosmetic changes (such as differences in paint or color/design of power base) does not warrant a new part.  This is not a wiki of historic part variations.  Exception: If the manufacturer designates a new part number for something, then it _should_ also be included as a new part here.  For example, the Ninco 10114 Starting Grid is identical to the 10103 Half Straight, except that it also has starting grid paint (which one could fairly argue provides a functional difference).  Thus, because the Starting Grid has its own part number, it is added here as a separate piece.  Yet, on the other hand, there are two different versions of the 10114 Starting Grid -- the older one has thinner paint lines and less staggered grid marks -- the newer one was introduced circa Ninco's N-Digital line.  These two versions should not be entered as separate parts.  My personal preference is to update the paint to the latest version, unless it is either a rare version, or is only a minor change that might look worse on screen.  For example, Ninco changed their Lane Changer paint from separated-red-white silkscreening to red-on-top-of-white silkscreening.  In this app, the older way looks better on screen -- especially when you alternate the draw order of the red/white striping (see the Ninco 10111 Crossover [that I have yet to update] for how muddy it can look when you don't alternate the red and white Z order).


## [v2024.1] - 06MAR2024, 01APR2024, 03JUL2024 MJJ
### Breaking changes (removals)
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


## [v2008.1] - 29JUN2008 MJJ
- Added all currently known N-Digital track pieces.
- Added all off-road and snow track... with color!
- Smoothed the crossover lines a tad.
- Not sure when: Updated the finish-line art on 10101 Starting Straight.


## [v3.0b] - 05NOV2005 Original
- The original `Tracker20.df3` found in Tracker 2000 V3.0b.

## v2.1 - 08JUN2004
- `Tracker21.df3` and earlier versions are not included in this repo.


## Other

Hint: To make red/white striping display the best on screen (if you care), alternate the order you draw/create the red and white polys (or post-edit the file in a text editor to do the alternating).  That way, it alternates which outline draws on top, giving better balance between the two.  I should maybe go back and do this for the Ninco 10111 Crossover like it did the others (removing the background, adding white polys between the reds, and alternating from the middle out).

I wonder if I have all the lanes backwards....?
