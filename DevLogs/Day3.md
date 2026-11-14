# Dev logs/diary, Day 3

## Update 1: 08:55 GMT+8

### It always crashes when no-one's looking
Went to sleep last night around 23:30pm after preparing enough tasks to keep Claude Code busy overnight, woke up a few times overnight briefly to check the screen was still on and had what looked like the expected console visible. Found out this morning at around 07:00 after actually checking the screen contents to find that my PC had once again crashed.

### Crash diagnostics & attempts at mitigating crashes
Like the Day 1 to Day 2 overnight run, both happened after around 30-60 minutes of inactivity (no user mouse movement). Attempting to determine and address the cause is difficult as there were multiple plausible causes and overlapping patterns, such as both times Claude was waiting for the 5-hour window reset, I stopped using my PC (no mouse or keyboard inputs), and powered off 3/4 displays (2 virtual also disconnected). This time PBO settings are less likely as I have set the system to the same "safe" state as that used for running overnight remote backups with almost no PBO2 per-core adjustments. Also can't rule out nvidia driver issues as that was updated a few hours before the MegaJam to deal with a bug affecting UE, or some part of my PC's power delivery side failing (all but one screen off, most CPU cores idling, nothing new being rendered on-screen).
This leads to one lead that could be tested right away:
1. Claude's scripts supposedly include something to prevent the PC from going to sleep, which could be clashing with my sandbox setup.
2. Enable the sandbox's experimental feature to prevent attempts at changing power related settings.

I enabled #2 above, which if the crash was caused by #1, should in theory work, then went back to sleep after restarting the PC and making sure Claude resumed. Woke up an hour later to find nothing crashed during the 1-hour idle. Not the most reliable test, but at least 1-hour is around 2-3x the length of time I've left my PC alone outside of sleep hours during this MegaJam. Will find out during the "Day 3" overnight run tonight if this was the solution.

I have now lost 14.5 (7+7.5) hours worth of Claude run times (excluding 5-hour usage limit waits) at this current stage of dev.

I can only hope the parallelism increase (at the cost of faster token usage) can offset enough time loss to finish enough for the MegaJam submission.

### Current game state:
- Rough Core mechanics implemented, Claude currently working on fixing bugs and adding a few features to help further separate PillowTalk from other existing games
- Graphics: still UE4 mannequins & prototyping level/walls/blocks from the default UE selection (placeholders).
- UI: at around the level of a low-cost or free content asset pack on the Epic Marketplace/Fab.
- vFX: minimal, all based on basic building blocks (placeholders)
- SFX: None
- Music: None
- Multiplayer (LAN): fully working
- Input support: Mouse, Keyboard, Controller, all working.

### Progress vs original schedule:
Almost on track, behind on the day 2 overnight run schedule.
Fortunately

### Today's plans

### Random thoughts
The current system/dev-framework in place for PillowTalk can easily be used to keep upgrading it post MegaJam. It is working fantastically so far. As long as I keep iterating on what it's doing. It could easily be taken, cleaned up and modified for any future game I want to make or program. In some ways this from-scratch solutions is starting to slowly resemble the development setups of large projects that run on large projects (agentic), just on a single-PC level and heavily capped by Claude usage limits.

#### A fun twist of fate (unintentional):
I had to call what would normally be called the `Director` Claude session `Conductor` to sidestep using the same word as the MegaJam theme to reduce the risk of unintended confusion during dev process. At the time I was designing all of this with Claude's help, the term `Orchestrator` escaped my mind and that was probably a good thing. I would interpret the meaning of an "Orchestrator" as working at a much larger scale than just a `Conductor` or `Director`. The `Conductor` would work on the design and refinement of my design and features, then spawn `Workers` to handle the low computation requirement tasks using Sonnet 5.5 models (can talk about this now as it's day 3).
For the parallelism improvement, I separated out the tasks that should not clash and then independently created 2 new `Conductors`, one for each.

Behaving true to the name `Conductor`, their roles are all focused on following through with my design, or perhaps I should call it my score? Like real conductors for compositions they conduct and the composition's author is reachable, they would consult with the author for parts of the score that needs work, could be improved upon or improvise.

With the way things are progressing, my role in PillowTalk's development has settled into something closer to the score composer and performance director. The orchestral theme is going strong.

Now I need to find a way to name the `Workers` something orchestra related. A `musician` does not fit, while a `Player` risks context corruption given that actual game players are frequently referenced in the design. Perhaps `Performers` would be suitable, but would that change how Claude interacts with the delegation process over the long term?

This is a stark contrast to the original PillowTalk game I tried to make and failed. I took on the role of everything, from the most tedious tasks, all the way through even single role involved in game design other than creating new art such as 3D models, drawing textures/artwork and creating sound/music; for these I went and purchased pre-made assets from the Epic Marketplace/Fab and from DAZ Studio.
The only things that carried over from the original PillowTalk to here would be name, rough concept and also re-using some of the assets I purchased for the original game's use (and the game that failed before PillowTalk original). But instead of being bogged down with an overwhelming number of tasks meant for a whole dev studio, I can focus on designing and directing the changes as long as they can be properly communicated to Claude, then working through issues and debugging.

09:45 GMT+8. Time to continue with the manual tasks.