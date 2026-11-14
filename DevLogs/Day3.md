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

## Update 2: 10:00 GMT+8
Turns out I hit my Claude 5-hour usage limit around 30mins ago, have to wait another 2 hours before Claude can resume.
Time to catch up on the manual work.

## Update 3: 10:50 GMT+8
Took the chance while the sandbox environments are being used by UE related tasks to create optimisations and fix:
- UBA: can now write out of the sandbox to cache folders (faster caching, less unnecessary recompiles, less warnings/errors)
- ZenServer: Running ZenServer outside of the sandbox was not enough. Direct access to the LocalDDC folders was also required for functionality. Made sandbox adjustments so Zen/LocalDDC can read/write faster.
- UE CrashReporter: often crashes, may have addressed. Sandbox env + long folder paths led to many unnecessary CrashReporter crashes, while CrashReporter was reporting on crashes and in turn crashed itself.
- UE LiveCoding sandbox optimisations
- UBT sandbox optimisations
- Temp folder write optimisations
The above combined should reduce the quantity of (non-fatal) errors and significantly speed up the whole ClaudeCode + UE-in-sandbox setup.
- Made some env security adjustments
- Reduced Build, Cook & ShaderCompile disk I/O bottlenecks
- Free'd up space for Claude Code & UE
Made good use of the Claude downtime to carry out these "offline" maint changes that were not able to be made safely while Claude and UE were running.

## Update 4: 15:30 GMT+8
It was exciting to watch the boss mechanics being tested by Claude Code on auto. Can't wait to run manual play tests once it's safe to do so!
Spent the last few hours doing background related tasks.
UNVEiL is now UE 5.9.0 Preview 1 compatible and debugged.
Created a set of reference MegaScans & Fab Quixel shared materials (unchanged, only imported + tested) & confirmed they work as expected.

## Update 5: 16:10 GMT+8
Took the whole automated development setup with the `Conductor`s offline for a performance (project/Claude docs level) maint in hopes of reducing token consumption.
Also taking this chance to install the UNVEiL plugin into the project and have Claude use it as necessary.

## Update 6: 18:05 GMT+8
This update took a long time and I have not yet addressed the `KnownProblems.md` that needs a manual pass + manual test and bug reports. Can't delay any longer, will bring the main `Conductor` dev back online.
Each Claude Code session's initial token usage should drop drastically now that the critical files have been optimised.
Currently around 6-8 hours behind design schedule. The time lost has been partially recovered, however need to aim to be way ahead of schedule. On schedule isn't enough.

Rebooted dev PC, recovered 6.4GB of RAM. Windows defender alone was taking up almost 700MB+ for the main executable.

## Update 7: 19:50 GMT+8
Many changes and fixes happening in parallel.
UNVEiL updated so the new MCP implementation will work properly with automated dev.
`Conductor` is working faster than I can type up the text for the new feature(s) that I would like to add (wow!).
This is a mix of most of the necessary core and extended gameplay features being finished, as well as effects of the changes from Update 5 & 6.
The actual gameplay Level design is completely behind schedule, need to start after this.
Game mechanics are a lot of fun to test now.
Need to document up bugs/issues for `Conductor` to fix (I can't keep up with it's pace, fantastic!).
(20:15 GMT+8) forgot to commit this.
Also kept forgetting to fix the +/- value issue with "DP" that I made during the intial design writeup phase, addressed and added as an upcoming fix.

## Update 8: 20:20 GMT+8
Fixed a Build folder naming issue, non-critical but it will affect archiving & proof of builds, so requries a date and time entry here.
