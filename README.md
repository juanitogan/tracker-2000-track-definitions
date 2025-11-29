# Tracker 2000 Track Definitions (parts file)

![Tracker 2000 - Track Definitions Editor screenshot](/wiki-images/T2K_Track_Definitions_Editor.png)

**NOTICE:** To be clear, **this is not the Tracker 2000 app.**

This repo is only for keeping [Tracker 2000](https://web.archive.org/web/20061230041821/http://www.slotrace.com/tracker/info.html) alive by providing updated track-definition files (the `Tracker30.df3` file).

The Tracker 2000 app was [abandoned in January 2007 ](https://web.archive.org/web/20070105133305/http://slotrace.com/)by its creator, Edwin of Slotrace.com.  You can download it from archive.org (the demo version _is_ the full version, minus the unlock code):

https://web.archive.org/web/20061231174222/http://www.slotrace.com/tracker/download.html

You can find an unlock code on the internet (this repo will not provide any unlock codes).  Note that "abandonware" is a made-up term and the properness of using such a code is up to you.  As far as it is known, the current ownership of Tracker 2000 is unknown and there is no one accepting payment for copies of it.  Regardless, this repo will not, itself, distribute copies of it.  The only focus here is the user-defined content file and/or files.

### Why? ###

When I first got my Ninco N-Digital track, Tracker 2000 was the best of the track designers at the time for Ninco... and still is the best among the free/abandoned choices -- primarily because **it is a linear editor rather than a 2D editor** ("D'oh!" say the others).  My club, Giant John Slot Car Racing (and board gaming, and food club), still uses Tracker 2000 for all our design (we take turns designing a new track every 2-3 months).  I have updated the track defs over the years to include all the Ninco 1:32 pieces I know of, including N-Digital (even though Ninco 1:32 currently a thing of the past).  It is time (overdue, really) to share that work (and other Ninco intel) with everyone else to help keep Ninco track alive.  (I say as I await some Scorpius digital gear to arrive to replace/upgrade the N-Digital stuff.)

Yes, Tracker 2000 is a severely outdated app from the Windows XP era.  But it still runs fine on modern Windows (other than the handful of poor UI decisions it was first built with--which take a tiny bit of getting used to).  It is unfortunate the source code was not released as I would be happy to fix many of those quirks.

![Tracker 2000 - Ninco N-Digital track example](/wiki-images/T2K_Ninco_Example_GJC_Nov2024.png)

### What else? ###

The wiki here contains both tips for using Tracker 2000 and a list of known bugs in Tracker 2000.  The goal is for the wiki to also contain hints and tips on the various tracks and systems.  For example, I have much to share about what I've learned about Ninco N-Digital and this will currently be the primary landing page for that.

[**➡️ Jump to the wiki.**](https://github.com/juanitogan/tracker-2000-track-definitions/wiki)

## How to use ##

- Backup/rename your current `Tracker30.df3` file in your Tracker 2000 folder.
- Download one of the `Tracker30.df3` files from this repo and copy it to your Tracker 2000 folder.

## Included Track Systems ##

| Brand | Scale | Current as of* | Last updated |
|-------|:-----:|:--------------:|:------------:|
| Airfix                   | 1:32 | pre 2007 | pre 2007 |
| Artin                    | 1:32 | pre 2007 | pre 2007 |
| Aurora                   | 1:64 | pre 2007 | pre 2007 |
| Aurora AFX               | 1:64 | pre 2007 | pre 2007 |
| Aurora MM                | 1:64 | pre 2007 | pre 2007 |
| Aurora Ajet              | 1:32 | pre 2007 | pre 2007 |
| Bit Char-G (micro RC, 0-lane) | 1:64 | pre 2007 | pre 2007 |
| Carrera Exclusiv         | 1:24 | pre 2007 | pre 2007 |
| Carrera Universal        | 1:32 | pre 2007 | pre 2007 |
| Carrera Exclusiv PRO-X   | 1:24 | pre 2007 | pre 2007 |
| Custom Routed            | 1:24 | n/a      | pre 2007 |
| Custom Routed Metric     | 1:24 | n/a      | pre 2007 |
| Fleischmann              | 1:32 | pre 2007 | pre 2007 |
| Granite Archer Raceways (4-lane) | 1:64 | pre 2007 | pre 2007 |
| Ninco w/ N-Digital       | 1:32 | ~2017    | 2025     |
| MaxTrax (4-lane)         | 1:64 | pre 2007 | pre 2007 |
| MaxTrax (6-lane)         | 1:64 | pre 2007 | pre 2007 |
| Marchon                  | 1:64 | pre 2007 | pre 2007 |
| Polistil                 | 1:32 | pre 2007 | pre 2007 |
| Revell / Riggen          | 1:32 | pre 2007 | pre 2007 |
| SCX / Scalextric         | 1:32 | pre 2007 | pre 2007 |
| SCX Digital              | 1:32 | pre 2007 | pre 2007 |
| Scalextric Sport Track + Digital | 1:32 | pre 2007 | pre 2007 |
| Scalextric Micro         | 1:64 | pre 2007 | pre 2007 |
| Strombecker 1:32         | 1:32 | pre 2007 | pre 2007 |
| Strombecker 1:24         | 1:24 | pre 2007 | pre 2007 |
| Super                    | 1:24 | pre 2007 | pre 2007 |
| Tomy AFX                 | 1:64 | pre 2007 | pre 2007 |
| Tyco                     | 1:64 | pre 2007 | pre 2007 |
| Vario (4-lane)           | ?    | pre 2007 | pre 2007 |

\* Last in production.

Note that 1:64 scale is commonly referred to as HO scale in the slot-car world, but HO scale is actually 1:87, and 1:64 is S scale.  Go figure.

No train tracks?  Bummer.  Yeah, okay, the software doesn't support railroad junctions and multiple routes easily.  Possible (as seen with digital slot setups) but not the focus.  Tracker is linear editor, remember?  Trains are best with a non-linear editor, or a branching linear editor.  Maybe I'll add my Lego train tracks someday (the only trains I own).  What about [Mini 4WD](https://en.wikipedia.org/wiki/Mini_4WD)?

## Style guide ##

TODO (track paint, picker order, etc.)

## TODO list ##

- Instead of providing one, fat `Tracker30.df3` file, which may be a challenge to diff and merge (not likely, but, meh), break it up by brand/system/type and provide a tool for merging them as wanted.  This will have the added benefit of making it easy to then also allow for creating ad-hoc hybrid sets for designing hybrid tracks (e.g. Ninco + Policar).  (Will likely need to insert a dummy part for odd-numbered sets to keep the picker pretty.)

#### TOnotDO ####

- I have considered adding border pieces as their own track def to help track their use better.  (Because Tracker is not flexible enough with borders to support start/end pieces, half pieces, and so on.  Not to mention inventory.)  But... this software doesn't support combining different track types--not even as a new track in the same design... even though adapter pieces are common between track types.  Thus, they would have to be an expansion the Ninco set... making it very big... sigh.  Also, again, the lack of support for non-ambidextrous curves will be a confusion point for the user (using/inventorying start/end pieces, also the inside/outside thing).

- Tracker 2000 does not color-code track pieces (an idea that came later in history).  In theory, one could add this feature by adding colored polygons on top of the track shape (like I do for snow and off-road track with Ninco)... but that sounds like maybe more work than it is worth.  But others may try it.  In which case, the tool might be expanded to make it easier to swap color-coded and non-color-coded track defs in and out.

- Changing the red track paint to another shade of red has been considered to keep Tracker from autocoloring it to other lane colors (like it does with lanes 3+, and left/right red/green curve swapping).  But I have not done this thus far because the color picker is very limited in color shades, leaving only dark red and pink as the other red options.  I could enter any red shade via text editor... but then that becomes difficult and mysterious for others to understand what is going on and to duplicate and/or maintain.  Thus, I'm letting this one be and it is what it is until a better color picker arrives (which will be never).
