# Dev logs/diary, Day 4

## Update 1: 05:45 GMT+8
Finally able to go sleep.
Queued up a lot of work for Claude overnight, should run stable now with enough work and enough parallelism setup.
Looking forward to seeing the results after sleep.

## Update 2: 11:50 GMT+8
Woke up to check and make sure PC hasn't crashed.
PC running and ok. `Conductor` finished ALL queued features. That was unexpected.
Asking claude to check

## Update 3: 15:55 GMT+8
Managed to get around 5.5 hours of sleep excluding getting up to check on the `Conductors` and adding new features & fixes to the queue.
This is technically the first update for my last "day" of the MegaJam 2026. Looking good so far!

## Update 4: 16:25 GMT+8
Definitely fun to play test!
Started bug logging for the polishing and balancing phase
Graphics assets need to be added today, and any final set of features finished

## Update 5: 19:50 GMT+8
So much to do and so little time left.
All of the gameplay features other than the attempt at DLSS has been implemented.
Level still incomplete, assets ready to be replaced.
Still yet to run a proper manual debug + provide Claude with the list to fix.
SFX can do with some updates.
Music missing.
Animations need replacing (TBD).
Character models need replacing (not started).
Couple of things I would like to add but don't have time.
Gameplay recording and video not done.
Draft for submission needs updating.
I am the bottleneck now, Claude is hardly running, trying to address this.
The fatigue from the 3+ days of intense dev + lack of enough sleep can definitely be felt.

Updates today will be sparse, not enough time.
Will most likely just commit hashes going forward until something needs mentioning here.

## Update 6: 21:30 GMT+8
- The whole multi-conductor + workers setup is starting to creak when I am involved and time is limited.
- First time I've seen Claude Fable 5.2 incorrectly reference this setup.
- They work well together if no restarts are made and I communicate with them via the "proper means".
- Attempted to create a separate AssetCreator with internet access allowed, too risky, not enough time, shelved. Fortunately current existing working setup limits all of their internet access enough to not need to worry. Just no way to ask for web searches for better posing for attempts at making new animations; it'll have to work from memory.