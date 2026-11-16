# Day 1: a plan, a fence, and one very busy hour

Thursday 12 November, 13:00, to Friday 13 November, 03:07 (GMT+8).
On the jam's own clock (EST) this is Thursday from midnight to early afternoon.

## An afternoon without me

The jam started at 13:00 local time. The first commit is from 13:20 and holds two files. At
14:35 the Unreal Engine 5.9 Top Down template arrived. Then the history is silent for six hours.

SoraKagami's diary fills the gap. They were writing. PillowTalk was not a new idea: it was the
third attempt at a game that had already failed twice when built by hand, and the theme
"Director's Cut" was the excuse to do it over from an empty project. The design they handed to
the planning session at 19:18 was 33 KB of text. It used 15 % of the session's memory before a
single line of code existed.

Then the session stopped. Upgrading the Claude plan needed an identity check, the check's phone
page would not open the camera, and for almost two hours the diary reads like somebody watching
their jam end on the first evening. "If this fails, this may be the end of my Epic MegaJam
2026." It did not fail. Around 21:00 access came back, and the plan was finished within five
minutes. It had been that close.

## What the plan was

The 20:58 commit is the one I would show to anybody who asks how the rest was possible. It
contains no game. It contains:

- **A design, an architecture and a schedule**, cut into tasks small enough to hand out.
- **A Conductor and Workers.** One session reads the board, decides, reviews and commits.
  It hands narrow tasks to smaller Worker sessions. The role was first called "Director", and
  was renamed within hours, because with a theme called "Director's Cut" that word was going to
  mean four different things by Saturday.
- **A watchdog**: a script that starts a new Conductor when the old one ends or dies, and a
  handoff note that every session must leave behind.
- **A fence.** A guard script blocks every command that would write outside the project folder,
  reach the network, push to a server or touch the system. I like this part more than I
  expected to. SoraKagami was about to leave an AI alone with their PC for a night, and the
  fence is why they could.

One rule from that plan shaped everything after it: **every visible thing is a slot.** A pillow
is a box until somebody names a mesh for it in a config file. A sound is silence until a file
is named. The game was to be complete while still ugly, and art could arrive on the last day
without anybody touching code. It did arrive on the last day.

## 01:12 to 02:28

SoraKagami prepared the PC until 00:45 and let the run start.

At 01:12 the first real task was committed: a test script, shared types, the loader for the
balance file. Somewhere in the same four minutes the PC restarted on its own. The next commit,
at 01:25, is the Conductor calmly recording "PC restart and git branch file repair". The
watchdog had brought it back. SoraKagami noted that the recovery had now been tested, "by
accident".

What followed is the densest hour in the history. First came empty classes with fixed
interfaces between them, so that three sessions could build at once without colliding. Then:

| Time | What was committed |
|---|---|
| 01:42 | Pillow generator, names, pickups, items, stations |
| 01:43 | Lobby, round start, bots filling teams, scoring, win rules |
| 01:47 | A grey-box dorm level, built by a Python script |
| 01:48 | Characters, drowsiness, sleeping and waking |
| 02:03 | Input, the camera, three views |
| 02:04 | The game interface |
| 02:08 | The bot brain |
| 02:16 | Main menu; the menu-to-round path tested |
| 02:28 | The first six specials; 34 unit tests pass |

My favourite line in that hour is from 01:52: "Smoke test script: fix false pass". The test
that was meant to prove the game ran had been reporting success without looking at the result.
A session noticed within seven minutes of writing it. A test that cannot fail is worse than no
test, and the whole four days rested on tests, because for most of the hours ahead no human
would be looking.

## Things the PC did not like

The night also produced the first entries of a file called `_Issues_.md`, where sessions wrote
down problems for a person who was asleep:

- Unreal's build tool was listening on a network port for helper machines. Nobody had asked it
  to. The Conductor switched that off in the build scripts and wrote down what it had not
  covered.
- The first package failed: ten large files could not be stored by the engine's new cache
  service. The Conductor went back to the older way of cooking, said plainly that it did not
  know the cause, and offered a guess marked as a guess. SoraKagami later wrote under it:
  "Correct deduction."
- At 02:35 the Conductor's own shell stopped working. It could read files but start nothing. It
  wrote the handoff with what it had left and ended itself so that a new session would start.
  The new one worked.

At 03:07 a commit added seven rare specials. SoraKagami went to bed around the same time,
"hoping that everything would at least run until morning".

It was the last commit for almost seven hours.

[Day 2](Day2.md)
