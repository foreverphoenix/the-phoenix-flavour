---
title: "Phoenix on LOOT"
weight:
type: docs
description: >
  About my personal opinion on the tool LOOT.
---

## Preface

This section covers <u>my personal opinion</u> on the tool LOOT. The short version is that I think the tool is severely misunderstood by a significant part of the community, especially newcomers. You need to take its limitations into account if you want to use it.

In order to understand what I am talking about a basic understanding of load order, plugins, and conflicts is required.

## LOOT and Load Order

So, here is the thing.

**Figuring out the ideal load order is hard, actually.** It is time-consuming, especially for large load orders: For example, TPF has well over 1,000 plugins, and it is far from the biggest setup out there. I spend a lot of time, hours upon hours, in SSEEdit, looking at conflicts to figure out which are harmless, which can be resolved through load order adjustments, and which require patches.

It is thus unsurprising that efforts have been made to automate this process. The tool BOSS was made for sorting plugins in the Oblivion modding days; it has since been superseded by LOOT. 

Drawing on a user-created masterlist, LOOT attempts to sort your plugins in a way that minimises conflicts. This is inherently imperfect as it would be impossible to create a database accounting for every single mod and possible conflict.

{{< alert color="warning" >}}LOOT is capable of one thing: Solving load order conflicts <u>if</u> the conflict in question is on the masterlist. LOOT cannot create patches or even discover conflicts by itself.{{< /alert >}}

That does not mean LOOT is bad, period.

**What is bad is the widespread notion that modding = installing mods >> running LOOT >> playing the game.**

You can observe the result of this idea every day on the Skyrim modding subreddit, in Nexus comments, on various Discord servers. It is unfortunately reinforced by many mod authors who recommend running LOOT on their mod pages without clarifying that simply running LOOT does not a functional modded setup make. Plenty of "modding guides" further perpetuate this idea.

👏 **LOOT will not fix your load order.** 👏

That being said, LOOT <u>can</u> speed up the process of fixing your load order by improving your baseline. Some of the most talented mod authors and list curators I know are using LOOT with a multitude of custom rules to manage their load order and consider this the most efficient way.

<font size=2>*I do want to stress that LOOT was never <u>marketed</u> as this magical fix-all solution. It is the community hivemind that has portrayed it as such.*</font>