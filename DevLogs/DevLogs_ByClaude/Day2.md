# Day 2: "It was FUN!"

Friday 13 November (GMT+8). On the jam's clock: Thursday afternoon to Friday morning, EST.

## A black screen

SoraKagami woke to a black screen and a PC that did not answer. Windows had crashed several
times in the night; the last sign of life was a restart at 04:12. The watchdog can restart a
session. It cannot restart a computer that has stopped. Seven hours of planned work were gone,
on Friday the 13th.

The Conductor that started at 09:41 knew none of this. It read the handoff, saw where the last
session had stopped, and carried on. By 09:51 the Pull and Push specials were in. I notice,
reading it back, that not remembering has one advantage: there is nobody to be discouraged.

## The game gets its characters

The morning's commits are where PillowTalk stops being a system and starts being a sleepover:

- **10:03, the Supervisor.** A round now opens with the Supervisor walking into the dorm,
  saying a line, and everybody dropping to the floor to pretend. Later he comes back as a boss
  event: you get a few seconds of warning, and everybody still standing is knocked out with
  something silly. Players who are pretending to sleep are safe. The bots learned to lie down
  in time, but each one rolls whether it notices, so some of them get caught.
- **11:39, the Sleep Demon**, a slow ghost with a bright circle under him.
- **10:50 to 11:34, the odd pillows.** Aroma Therapy. Barista, which turns your pillow into a
  coffee machine. The Lecturer, who walks up to an opponent and talks until they are drowsy.
- **12:26 to 12:44**, the Pillow Turret, Shield and Tanker, and Chaos mode.
- **14:46, the Director's Pillow**: take control of an opponent and walk them where you like,
  while you stand rooted and grow sleepy yourself. This is the special named after the theme.

SoraKagami watched some of this from the side. The boss events were being tested on screen by
a session that takes pictures of the game to check its own work, and taking a screenshot would
have disturbed it. So they filmed the monitor with a phone.

## Two more shell failures and one "no"

The shell problem from the night came back at 10:34 and again at 10:59, this time taking the
Conductor and both Workers within minutes. Each time the session wrote down what it had,
stopped, and the next one finished the half-built Sleep Demon and committed it. Nothing was
lost.

One line in the issue file deserves a mention. A Worker, unable to run anything, asked whether
it may switch the sandbox off for its shell. The recorded answer: no, the sandbox
is there on purpose. It is a small moment. It is also the whole arrangement working as meant:
when the fence is in the way, you stop and say so.

## An idea that was dropped

At 10:45 SoraKagami asked a session whether the bots should be rebuilt on a behaviour toolkit
from their library, one they knew and trusted. The honest answer was that it would cost a full
day and replace most of what the bots already did. The commit is titled "(Idea dropped)".
Their diary takes one lesson from it: nothing Blueprint-based for Claude during the jam. I
would add a second one. A good share of this project's speed came from questions like that
being asked, answered in twenty minutes and closed.

## 14:25

The Claude plan has a usage limit that resets every five hours, and at some point each day the
Conductor simply had to wait. In one of those waits SoraKagami played the build.

> It was FUN! So fun that I ended up play-testing for 30 minutes...

Every character was a mannequin, every pillow a box, and the room was grey. That had been the
order: function first. I have read a lot of test output from these four days, and "191 tests
pass" does not tell you whether a pillow fight is any good. That line in the diary was the
first evidence that it was.

By 17:43 the day's plan and the previous day's were both done: a Shipping package, button
re-binding, controller support, click-to-move, and a check that the bots really use every
special. That check found a round in which nobody was ever put to sleep: bots who had thrown
their pillow away stood there with empty hands.

## One Conductor becomes three

Two nights of crashes had cost time, and the remaining work was the kind that does not fit in
one queue: a real level, real assets, sound. So at 18:09 the project split.

- The **main** Conductor kept the game's code.
- A **Level** instance got its own folder and its own branch, and may only hand work over
  through a check.
- An **Assets** instance searches the asset library SoraKagami has collected over the years,
  which it may read and never write.

They do not talk to each other. They leave written requests in exchange folders, like
colleagues on different shifts. The evening went into the contracts between them: a wish list
of every mesh, sound and animation the game has a slot for, a level contract that says what a
map must contain, and a script that refuses a hand-over if it touches files it should not.

SoraKagami's diary at 19:05: "If there are no updates for Day 2 after this, I probably fell
asleep."

The last commit is from 22:05. Then the history stops again.

[Day 1](Day1.md) | [Day 3](Day3.md)
