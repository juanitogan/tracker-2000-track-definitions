# Tracker 2000 Track Definitions

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


## TODO list ##

- Instead of providing one, fat `Tracker30.df3` file, which may be a challenge to diff and merge (not likely, but, meh), break it up by brand/type and provide a tool for merging them as wanted.  This will have the added benefit of making it easy to then also allow for creating ad-hoc hybrid sets for designing hybrid tracks (e.g. Ninco + Policar).

- I have also considered adding border pieces as their own track def to help track their use better.  (And, not to mention, Tracker 2000 is not flexible enough here to support start/end pieces, half pieces, and so on.)

#### TOnotDO ####

- Tracker 2000 does not color-code track pieces (an idea that came later in history).  In theory, one could add this feature by adding colored polygons on top of the track shape (like I do for snow and off-road track with Ninco)... but that sounds like maybe more work than it is worth.  But others may try it.  In which case, the tool might be expanded to make it easier to swap color-coded and non-color-coded track defs in and out.
