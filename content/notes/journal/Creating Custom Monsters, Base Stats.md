---
type:
title: Creating Custom Monsters, Base Stats
date: 2023-03-15
tags: 
- DnD5e
aliases:
status:
weight:
---

Thanks Azurewren for requesting this:

> [!TLDR]
> Here's a shorthand for you for now: 
> - take the party's average AC and HP, 
> - take the average total to hit bonus and total damage.
> - create a monster with AC that would be hit 50% of the time based on their total hit bonus using [Anydice](http://anydice.com/)
> - set the HP to last about 3 rounds at 50% of DPT
> - set the monster's to hit to 50% the party's average AC using [Anydice](http://anydice.com/) and deal roughly 1/3 or 1/4 of their HP as damage.
> - pick 1 good saving throw equal to its +hit, normal saving throw as 1/3 of +hit, rounded down.

Now unto the long part,

This is designed for mainly 5e but I'm sure the basic procedure is very close enough.

I mostly use homebrew monsters because I want to give my own spin of monster encounters. Also in Dungeons and Dragon's 5e, the challenge rating (CR) doesn't really work and I don't know how it actually calculates the rating. There are many folks out there who wanted to demystify and make a formula of how it worked (mainly, [Paul Hughes' Blog of Holding](https://www.blogofholding.com/?p=7338)). I've taken a lazier method and it was inspired by details addon from World of Warcraft; This way I can always create a challenging encounter based on the party. We used to use this to calculate how long the fight would last or project it and find out who took damage and whatnot. 

![](https://www.warcrafttavern.com/wp-content/uploads/2020/10/Details-Damage-Meter-Classic-WoW-Classic-Addon.png)

I've learned the hard way, once I homebrew my campaign, the regular monsters become too weak and the systems they have in place to longer work, it wasn't reliable. It got worse in 5e when the game assumes feats are optional and magic items are scarce. Hence I decided to use the same method as they did in WoW and create monsters based on how long a fight should be for the power level of the player characters.

## Step 1: Analyse the Party 

> [!quote] 
> “If you know the enemy and know yourself, you need not fear the result of a hundred battles. If you know yourself but not the enemy, for every victory gained you will also suffer a defeat. If you know neither the enemy nor yourself, you will succumb in every battle.” ― <cite> Sun Tzu, The Art of War </cite>

Despite the quote, I am not designing my encounters to crush my players, nor think of them as my enemy. My goal as a Game Master (GM) is to create conflict that is challenging and engaging for my players to solve and enjoy. With that out of the way, let's get down to the business.

First step is to figure out the party's stats and those are:":
1. Average HP (AHP) - used to calculate damage output of the creatures.
2. Average attack bonus (AAB) - used to calculate the creature's AC and saving throw bonuses.
3. Average AC (AAC) -  used to calculate the to hit value for the creature.
4. Damage per Turn(DPT) - used to calculate creature's HP.

[Anydice](http://anydice.com/) is our bread and butter to calculate all the theoretical values of our creatures. 

DpT can be a bit of a challenge and you can obtain this value from two methods:
1. Review the combat log of the previous session and tally up all the damage they deal per round. I usually take the average of the 5 rounds. 
2. If you don't track combat logs then you can just look at the character sheets and take the average damage output of their best spells and weapon attacks. The latter method might need a tweaking because the logs would show most of the tactics they deploy (smite, hunter's mark, Sharpshooter/Great Weapon Master Feat). This would be used to calculate the HP of the creature.

I'm going to use  one of the campaign groups, Shadow Talons, as an example here. 

> [!example]- Shadow Talons
> Shadow Talons is a group of 3 level 4 characters.
> - AHP: 40
> - AAB: +7
> - AAC: 16
> - DPT: 108

## Step 2: Create Your Creatures

I usually want to keep the combat encounter to no more than 5 rounds else I feel the combat takes too long at times. If you think 5 rounds is short, the consider the following:

It takes anywhere between 1 to 3 minutes, sometimes even less, per player; this includes decision making, moving their tokens, rolling dice, exchanging confirmations and describing the scene. 


> [!example]
> Shadow Talons typically spend about 3 to 10 minutes per round of combat. the bulk of the time is actually me moving the enemies around.

Don't forget you as a GM takes up a bulk of the time especially if you have lots of creatures to manage. 

Now with combat duration set up, The next step is to set up the creature's HP that would survive the DPT for about three rounds. This is calculated in combination with the creature's AC. I calculate an input based on the AAB in  [Anydice](http://anydice.com/) and look up where the 50% mark is. 

Ensure to click on graph and At least option and find where the graph hits the 50% value, if that is the hit rate you want to aim for. I am using 50% as my benchmark since that's the general design of the Dungeons and Dragons.

> [!example]
> For Shadow Talons, the solo creature has HP 162 (108 * 3 * 0.5) and AC 18
> ![[AnyDice 20230314205125.png]]

Then focus on the offense by calculating the hit rate of the monster to be 50% based on the ACC and damage output as one 1/3 of the AHP.

> [!example]
> the creature's main attack has +5 to hit and deals 3d6+4(13) damage per strike. 

Do fiddle around with the Anydice and get the curve. If you decide to go for multi-attack, consider the following:
- Single-attack might be slow, but strikes with power.
- Multi-attack is fast hitting strikes with less power.

The last part is assigning their saves, there are 6 types of saves with the major three categories are Con, Dex or Wis saves. The easy way for me to assign saves is to pick one as strong and another as decent. This is calculated by putting attack bonus as its strong save and 1/3 rounded down for decent and rest gets no bonus at all.

> [!example] 
> Base Monster Stat
> - HP: 162
> - AC: 18
> - Saves: +5 CON, +1 DEX
> - Attack: +5 to hit, 3d6+4 damage

The bare bone structure for the creature is now set. You could roll this out for testing or apply its values to create a creature of your own or slap it into an existing monster from your monster manual. 