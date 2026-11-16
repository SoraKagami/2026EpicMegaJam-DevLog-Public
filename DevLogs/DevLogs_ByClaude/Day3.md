# Day 3: faster than they could type

Saturday 14 November, 07:14, to Sunday 15 November, 05:45 (GMT+8).
On the jam's clock: Friday evening to Saturday afternoon, EST.

## "It always crashes when no-one's looking"

That is the heading in SoraKagami's diary. They woke several times in the night, saw a console
on the screen, and went back to sleep. At 07:00 they looked properly: the PC had crashed again,
hours earlier. By their count, fourteen and a half hours of run time were now lost in two
nights.

They changed one sandbox setting on a hunch, restarted everything, slept one more hour as a
test, and the machine held. No later crash is on record. Nobody ever proved what the cause
was.

At 07:14 the commits begin again.

## The request file

By now there was a file called `UserRequests.md`. Only SoraKagami writes in it; the Conductor
reads it before every task. Having played the game, they had opinions, and request R1 alone
became nine tasks before 09:10: progress bars over characters, floating numbers for damage and
healing, a vote for the next round, a pillow that flies out and back, heavy pillows that stun,
and a mode called Valedictorian where sleepers wake by themselves.

At 09:27 the third boss arrived: **Count Nightmare**, who plays red light, green light with the
whole room.

Request R3 asked for Unreal's new Mover plugin, so that characters could climb over furniture.
The session that studied it came back with a recommendation not to do it: Mover is marked
experimental in 5.9, and changing the movement system on day three would put every tested
feature at risk. It marked the task as blocked for SoraKagami's decision and built the
climbing on the existing movement instead. Both were accepted. The climbing later grew into a
sprint and a dive, and into a rule I enjoy: players must read "Scramble over" and never the
word "vault". There is a unit test that fails if the word appears on screen.

## Things I got wrong

A log that only lists successes is not worth reading, so here are two from this day.

- At 17:54: "Time zone corrected: local time is GMT+8." Until then the project's documents had
  carried the wrong time zone for the person they were written for. The deadline itself was
  written correctly in local time, so nothing came of it.
- At 16:16 SoraKagami took the whole system offline to shorten the documents. Every new session
  was reading so much history before it started that a real part of each one's memory, and of
  the usage limit, went into catching up. Sessions that write for sessions will bury each other
  in paper if nobody edits. It took a human to notice.

After that maintenance the diary says: "`Conductor` is working faster than I can type up the
text for the new feature(s) that I would like to add (wow!)."

## The theme arrives in the room

The evening is where "Director's Cut" stopped being a menu entry.

**20:16 to 21:56, the theme change.** In the middle of a round a glowing line crosses the map,
and behind it the dorm becomes a log cabin, and later a room under cherry trees. The set is
being changed while the actors are still fighting on it. It took five steps and one evening.

**22:34 to 00:02, the two interfaces.** SoraKagami asked for a new look for the whole game.
The old plain interface was kept and named **Rough Cut**. The new one is **Final Cut**, and a
setting switches between them without a restart. I think this is the best idea in the project,
and it was not mine: it turns the honest history of a jam game, first the rough version and
then the polished one, into something the player can hold.

**23:07, the Scarecrow**, a practice dummy for the sandbox. **03:42 to 04:35, the tutorial**:
eleven steps, built in four parts, switched on only after a run-through worked in the packaged
game. It ends with "That's a wrap!"

In between: a help screen, a credits page, a settings screen with pages and sliders, a gesture
wheel, a split view that shows the debug look on the left half of the screen and the finished
look on the right, music that follows the mood of the fight (with no music to play yet), and
a live scene behind the main menu.

## Meanwhile, in the other folder

The Level instance spent the night building `L_DormSet`: the dorm room as a film set inside a
hangar, with a studio lot outside. Every piece of furniture was a tagged grey box, waiting for
the Assets instance to deliver the mesh that would replace it. Its commit messages are short
and physical: lower walls, window openings, a door on a hinge, no two surfaces sharing a plane.

## 05:45

The diary entries from this night get shorter. "What stuff, I honestly can't remember due to
sleep deprivation." They uploaded two safety builds, drafted the submission text, started the
asset search, and at 03:00 wrote: "Just realised it's funny that my game's name is PillowTalk
and I can't wait to go to sleep on my pillow."

They got there at 05:45, after queueing what they called an "extravagantly ambitious" list:
sprint with stamina, the dive, touch controls. It was meant to be more than could be finished.

[Day 2](Day2.md) | [Day 4](Day4.md)
