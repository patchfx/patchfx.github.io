---
layout: post
title:  "Approaching Alpha"
date:   2016-11-28 09:00:00 +0100
---
Despite it being quiet here on the blog front, development on "Call the
Blacksmith" has been going really well. A whole raft of new features and the
main game loop is finally starting to take shape. In it's current form customers
(mostly peasants) come at random intervals to order items (also random). The
player can immediately start working on items or alternatively queue some orders
up and begin crafting at a time of their choosing. Crafting depletes inventory
and customers return to collect items once completed, rewarding the player with
money and XP.

# GUI
The majority of work this month has gone into the UI. They aren't so much hard to
write, just a little tedious and have lots of tiny little details that are
easily overlooked. The game is a little UI heavy given the management sim
features and getting this all in as early as possible has started to pay
dividends.

The game now has a HUD displaying the players currently level and progress,
along with some icons for orders, inventory, fatigue and financials.

<img class="img-responsive" src="/assets/hud.png" alt="Call the Blacksmith HUD">

# Crafting
The new crafting dialog features a drag and drop interface, progress bar and
success/failure depending on the item difficulty and the players current level
of expertise. I'm going to be introducing energy expenditure shortly as well as
managing the fire temperature, all which will have an affect on the resulting
item. In the current state it's fairly likely that the crafting is successful,
I'm planning on tweaking it more once I have a more refined game loop.

<img class="img-responsive" src="/assets/crafting_dialog.png" alt="Crafting
Dialog">

# Inventory
Artwork for the different kinds of resources used in crafting items is now in.
This removed a blocker with the inventory management and with all the backend
work I had done previously, it just kinda worked and was fairly simple to
complete. There currently isn't a way for the inventory to be replenished, but
I'm working on that in the current milestone.

<img class="img-responsive" src="/assets/inventory_dialog.png" alt="Inventory
Dialog">

# 0.5.0 Alpha
I had planned my milestones so that 0.5 would be the first publicly available
alpha-release. I'm just finishing up 0.4, so that isn't very far around the
corner. I'm pretty nervous about getting it into the hands of other people, but
think it's really important to do this as early as possible. If the core game
mechanic isn't fun, I'm going to waste months later on. Feedback is really
important.

For news about the alpha release and to get your hands on an super early copy of
the game, signup to the mailing list below.
