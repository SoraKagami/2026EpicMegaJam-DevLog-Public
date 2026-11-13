# Dev logs/diary, Day 2

## Update 1: 09:55 GMT+8
Went to sleep around 03:00 GMT+8 after dealing with windows crashing, hoping that everything would at least run until morning.
Woke up to find my PC's screen completely black and system nonresponsive. Logs showed windows crashed a few times overnight and stopped logging sometime after a reboot at 04:12.
Last commit by Claude was at 03:07.
7 hours of potential work lost due to a combination of hardware failing and windows crashes.

There is still hope, the relaunched Claude Code has started play testing some of the basic concepts and at least something has been produced.

## Update 2: 10:45 GMT+8
Had a random idea to ask a Claude Code session to investigate whether it is better to continue using PillowTalk's current Bot AI system, or perhaps look at maybe using a premade one that I have in my Fab library "AI Behavior Toolkit" (AiBT for short), which I have used in the past and worked well. Given that no C++ code was in AiBT, Claude only had a superficial look making guesses based mostly on filenames. It didn't even start up the editor (so no MCP use).

Claude's response was pretty much that we would need to make too many changes to existing code to even start using it; which sounds like the whole gameplay system's player/bot related aspects. The time estimate was a full dedicated day of editor work just to add PillowTalk's existing features to AiBT.
It was way too late for me to have thought of this.

There were still some gains. The session then suggested some upgrades we could make after reading only the filenames from AiBT. Probably from it's own inference memory of how other AI bots were implemented.

My takeaway: do not introduce anything blueprints based for Claude to work on, at least not for the MegaJam. The time cost is deemed too high.

Investigation results saved as a PillowTalk commit `51ed38635dff985846d7be032ab12a599c03ce7effc5c6c5933dfb16a71114e1`

## Update 3: 11:45 GMT+8

### Found old docs
Found the documentation and notes for the original abandoned PillowTalk game that I never finished. Saved the Gitea server url.

These docs won't be exported out until the end of the jam, may create hashes instead so there won't be a need to actually read the text by accident.

I do not want to poison my planning as current plans were made after I forgot all of this existed. Didn't even remember I had this self-hosted wiki section.
I don't want to have to credit features that are similar as something I planned before the MegaJam when it was completely and utterly forgotten.

They however can be used after the MegaJam to implement all of the differences that makes sense if the Claude Code built version is good enough to possibly release as an actual game.

Also found the pre-jam notes I made for preparing and saved them out in the private devlog repo. Will hash & commit hashes to Github as proof; file dates and commits are current however as they were manually extrated from my own personal daily notes/scratchpad/to-do.

### PillowTalk (remake) progress
Just saw a brief snippet of the test Claude ran. Not one, but both of the boss encounter features has been implemented. Exciting!
Attempting to screenshot would interfere with the image capture that Claude appears to be using to check progress (already tried, saw it repeat tests), so recorded using my phone.

### Figured out a way to speed up
Figured out two ways I separate out the dev path into parallel Claude runs on aspects that should have minimum interference beyond what it itself designed.

Will give the implementation a try after breakfast. If this works, I may be able to make up for the 6 hours lost due to the hard PC crash overnight.

### New Ideas-scratchpad.md
Instead of saving my notes in my usual daily notes/scratchpad/to-do file, the MegaJam related parts will be saved into this new Ideas-scratchpad.md in the private dev log repo to keep it's commit history public.