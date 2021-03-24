---
layout: post
title:  "Dota2 Heroes"
date:   2021-03-24
categories: blog
---

<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

# Dota2 Data Dive

## Intro
*Defense of the Ancients 2* (DotA 2) is a spectacularly successful multiplayer online battle arena video game by Valve that has taken off in the esports world, generating millions of dollars for players. Interestingly, it began as a MOD (!) in the massively multiplayer game *World of Warcraft* by Blizzard Entertainment, and then in 2013 *Dota 2* was released as game in its own right to the public. 

Somewhat like a complex, multifacted capture-the-flag, *DotA 2* pits two teams against each other to destroy the opposing team's home-base, known as the 'Ancient.' For each game, the map is the same, and there are routine and reliable mechanics that the players need to learn to leverage to their advantage, from monsters called 'creeps' spilling out onto the field toward home bases to purchasable items spawning in set locations. Each player has multiple roles. The map is rectangular, with the Ancients in diagonally opposite corners (bottom-left and top right), three 'lanes' that are open, grassy land between the Ancients, and 'jungles,' which are forested areas that players and non-playable characters (npcs) can hide in. Throughout the game, players gain experiene points and collect gold, and with that they level up, develop skills, buy items, and so on. It's a lot like *League of Legends*, if you've played that :).

## OpenDota2

Awesomely, players of *Dota 2* are pretty serious about their gaming, and enough so that an open dataset of *Dota 2* match, player, and hero data is available online at (https://www.opendota.com). 



## Hero Stats

Some beginning exploratory data analysis on the hero stats gives a glimpse of what the game designers have in view for the game. 

<img src="{{site.baseurl}}/assets/img/hero_corr.png">
Mind you, each game has a time limit of 40 minutes, so leveling up and developing abilities has to be something directed.

Perhaps unsurprisingly, we see some collinearity between a base attribute (e.g. base_str) and attribute gain (e.g. str_gain). Basically, if you start with a hero with a high attribute, then you should expect that by leveling up you'll increase the attribute more by level than if you were to get another hero less-inclined towards the attribute and level it up. 

Some other observations
* attack_range has absolutely 0 relationship with base_agi
   * so strange! in my favorite series *Final Fantasy*, AGI is a big thing for Rangers, who need high attack range!
   * in fact, attack_range is related to base_int -- ie for wizards nuking (casting spells)
   * also attack_range is strongly negatively correlated with str!
* move_speed is postively correlated with base_armor, so the higher the base armor (probably heavier you are), the more move_speed the hero is granted (probably to make up for it)
* projectile_speed is negatively correlated with base_attack_max and base_attack_min
   * gotta nerf the speed if the attack is high, huh??
   
Let's see if we can separate the Melee and Ranged heroes.