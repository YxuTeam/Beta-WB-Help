# Command Docs

Welcome to command docs, where all commands will be explained in depth.  
Make sure to read everything below so you can fully understand the docs!

## Prefixes

All prefixes of the bot are `w!, W!, w., W.`.

## Arguments

* `(arg)` - Required parameter that you must include in the command.
* `[arg]` - Optional parameter that you can ignore. Usually for providing detailed commands.
* `<arg1|arg2>` - You can enter either command 1 or command 2.
 
## Types of arguments

There is several types of arguments to use in commands, but we will talk about 4 in particular:

### User (or Member)

User is represented as a discord user. You can mention it in a command by different ways:
* **By hashtag:** Waza80#8017
* **By ID:** 959534223293833256
* **By mention:** `@Waza80` | `<@959534223293833256>`
* **By autocomplete**: Waza

### Channel

Channel is represented by a (most likely text) discord channel. You can mention it in a command by different ways:
* **By ID:** 1059904468398919740
* **By mention:** `#general` | `<#1059904468398919740>`
* **By autocomplete**: gen

### Role

Role is represented by a discord role. You can mention it in a command by different ways:
* **By ID:** 1034315703412592770
* **By mention:** `@sus` | `<@&1034315703412592770>`
* **By autocomplete**: s

### BanEntry

BanEntry is represented as a banned user in the server. You can mention it by different ways:
* **By ID:** 992949907981881425
* **By autocomplete:** WazaBot

## Autocomplete

Our autocomplete tool uses the [Levenshtein distance](https://en.wikipedia.org/wiki/Levenshtein_distance) to find the member which is the closer to the one you specified.
For example, let's say you want to find `@Maria420` but you don't have her mention. You can always do like this:

`w!find Mar` | Outputs "Maria" with a 3/5 accuracy.

It works with Members, Channels, users, and BanEntries.

> Notice: it may not work on all uses, for example:
> * Let's say there is Zac, and Margaret  
> ``w!find Mar`` | Outputs Zac with a 1/3 accuracy. [FIXED]

> * Let's say there is Waza80#???? and Waza80#????
>   ``w!find Waza`` will output the one with the lower hashtag.