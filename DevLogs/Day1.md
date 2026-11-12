# Dev logs/diary, Day 1

## 30mins into Epic's MegaJam 2026
SoraKagami here. I am working away from home, time-zone is UTC+8. Missing home (UTC-8), would have been able to wake and sleep at normal hours.

This is a lot for a solo dev. 30mins in and I am completely overwhelmed by tasks. Just created my game's empty repo, had issues sync'ing the repo to my own Gitea server (been having problems with git LFS since quite some time ago, never figured out what I did wrong). Finally got it sync'd. With only the `.gitignore` and `.gitattributes` in project.

Tried to finish writing the plan before starting, ended up going overtime and just copy/pasted my draft notes in (it's a mess!) for the ambitious part of this game (it's way more than I could hope to finish).

### Game Concept Summary

A fun multiplayer party type game. With a theme that doesn't appear to be used so far in other games, and re-imaging a bit of fun from our childhood days. I will document the actual gameplay and design later once things have progressed (perhaps day 3/4). Don't want to give my competitors (GenAI crawlers/bots) ideas right?

### Ambition

I took a game that I failed to complete (did not get far, it looks like a mess!), that I made because my previous game that I worked on for a few years got so complex and broken that I gave up and tried to take the usable parts to make a new smaller game with a tighter goal. Well, that didn't work, as what I tried to port over was so broken that, the few months I've spent trying to fix things, I could have shipped a demo of the game if I rewrote it from scratch.

With this Epic MegaJam 2026's theme being "Director's Cut" and with the livestream mentioning that we should be ambitious, especially given the crazy short time of 4 days, well... it just struck me I may as well try to re-create the 2nd failed attempt by taking the base general gameplay design and making it from the ground up using Claude Code.

The original 2 game attempts were all hand made, hand coded. It was absolutely overwhelming for a solo dev that started with zero game dev experience, no knowledge of Unreal Engine, and forgot how to code in C++. Oops.

On top of trying something that already failed, I expanded the design and gameplay scope a lot.
For now all I can do is document the repos and changes as hashes with timestamps and publish what I can to Github without giving away too much. For now.

If I were to be objective, in hindsight my first game was like a total novice trying to build a small turboprop plane from scratch with no knowledge nor experience, but ending up trying to build a fighter jet with the ambition to have it fly to space.
The second game was like trying to take the frames of a failed metal aircraft design that can't even fly and trying to turn it into a glider. It was so heavy it should have been designed and built from scratch.

### Proof of work

Made a quick script (thanks to Claude Code's help) to grab the commit hashes and dates from relevant repos then outputted them into `.log` files that I am publishing together with this repo.

### Random remarks/rant

The pre-made stuff I will be using for now are just a debug plugin (editor only tool) I wrote for the first failed game then upgraded during the second game's dev, and now it will most likely end up in this one to assist with debugging refs.

I will also be using another UE plugin I wrote from scratch (again with Claude Code's help) that I started a few days ago for asset management. When I finally decided to sign up for this competition, it dawned on me that it was near impossible to access the assets I purchased or claimed from the Unreal Marketplace turned Fab without spending days (Asset project upgrades, broken refs, deprecation fixes, shader compiles, space management etc.). Then there's the Epic Launcher issues on top of my slow internet connection.
The asset management plugin is called `UNVeIL`: an **UNreal Viewer for External and imported Libraries**. It won't have any direct impact on the game code as it is used solely to help with finding and importing assets that I already have on my PC.

65mins past the starting time. It's time to ask Claude for help generating the `CLAUDE.md` file, plans, docs etc. which I was unable to even prepare for.
Just managing/updating my own local server services, dealing with software updates, recent vulnerabilities and patching, creating UNVEiL and updating UE dev related tools took up all of my time for the last 2 weeks. Dealing with Windows, driver issues, and trying to keep my dying dev PC from actually dying cut into sleep hours; wish I could afford to upgrade the hardware. Dev PC's CPU's per-core PBO is climbing by the week for stability otherwise windows will crash on boot, server's i7-47xx CPU is so old I had to increase the voltage to keep it running. 1-2 years of tech debt!

**I am really excited at the prospect of actually finishing the complete ground up remake + upgraded version of my game**. The Epic MegaJam gave me a reason to just throw in the towel and move on, start fresh to try and see if GenAI can make up for my own shortcomings.
Based on my recent experience of using Claude Code to create `UNVEiL`, this is definitely possible.

## Update 2: 15:00 GMT+8 (2 hours into MegaJam)
- Created a blank top-down UE 5.9 project
- Updated `UNVEiL` (still incomplete, working on it!)
- Updated script `CommitHashLogger`

Forgot to mention above that `CommitHashLogger` was made to help with proof of work/time. Currently a private repo on Github, will most likely make it public at the end of the competition as it's a useful script.

Still have not had time to work on the game's CLAUDE.md prompt, plans, docs etc. Running 2 Claude Code instances simultaneously. Looks like I may have to move to three at this rate but honestly, 2 seems to be my multi-tasking limit (and sometimes my PC's too). The bottleneck is from the human side (me) most of the time, ouch!