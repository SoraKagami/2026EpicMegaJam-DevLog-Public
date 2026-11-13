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