# Guild Golem Discord bot

The Discord bot for [Guild Golem](https://guildgolem.com), a guild management site for WoW Forever. It puts your
guild's raid nights into your Discord server. Raiders sign up with buttons, officers post the groups, and people who
haven't answered get a reminder.

The bot's code is part of the Guild Golem website and isn't public. This repo explains what the bot does, what it
asks Discord for, and where to report problems.

## Status

Live. Any guild on [guildgolem.com](https://guildgolem.com) can add it to their server (below). It's updated along
with the site.

## Adding it to your server

1. Sign in at [guildgolem.com](https://guildgolem.com) with Discord and open your guild.
2. Open the guild's Discord page and link your server. A new guild can do this while it's being set up.
3. Discord asks you to approve the bot for that server. You need the Manage Server permission there.

A server can be linked to more than one guild, and a guild can move to another server later.

## Commands

Officers are the guild leader and the officers the leader lets post to Discord.

| Command | Who can use it | What it does |
|---|---|---|
| `/raid` | Officers | Posts a raid night's sign-up message in the channel |
| `/roster` | Officers | Posts a raid night's groups and bench in the channel |
| `/remind` | Officers | Mentions everyone who hasn't answered a raid night yet |
| `/nights` | Officers | Posts each raid night in the channel a few days before it (7 by default), or stops |
| `/logs` | Officers | Posts a summary in the channel when someone shares a combat log with the guild, or stops |
| `/recruit` | Officers | Posts in the channel when someone applies through the guild finder, or stops |
| `/patches` | Officers | Posts new game builds and Guild Golem's data updates in the channel, or stops |
| `/next` | Everyone | Shows your next raid nights, with buttons to answer them |
| `/away` | Everyone | Marks you away for some days, so your raid nights answer Can't come |
| `/talent` | Everyone | Shows a talent: what it does, its ranks and a link |
| `/spell` | Everyone | Shows a class spell at its highest rank, with its cost and cooldown |
| `/build` | Everyone | Shows a talent or Legacy build from its export string |
| `/help` | Everyone | Lists what the bot can do in the server |

Using the bot needs a Guild Golem account. Anyone without one is sent a sign-in link first.

## What it posts on its own

These only happen in channels an officer chose with the commands above:

- Raid night sign-ups, a few days before each night (`/nights`).
- A live post when someone in the guild is logging a raid live, edited when the raid ends (`/logs`).
- A summary of each shared combat log (`/logs`).
- New applications from the guild finder (`/recruit`).
- New game builds and data updates (`/patches`).

## Direct messages

Each player picks their own DMs in Account settings on guildgolem.com.

| DM | Starts |
|---|---|
| Reminders for nights you haven't answered | Off |
| Updates about your raid nights | Off |
| Loot you're handed | Off |
| Your guild's news, an application's answer, a leader's warning before a handover | On |
| Raid day: your spot, assignments and loot a couple of hours before a night you're placed on | On |

If Discord refuses a DM (closed DMs, or you left every shared server), the site tells you why they stopped.

## What it asks Discord for

When it joins, the bot asks for: Manage Channels, Add Reactions, View Audit Log, View Channel, Send Messages, Manage
Messages, Embed Links, Attach Files, Read Message History, Mention Everyone, Use External Emojis, Use Application
Commands, Manage Threads, Create Public Threads, Use External Stickers and Send Messages in Threads.

Today it uses a smaller part of that:

- Sending and editing its own posts.
- Replying to its own posts with reminders. Replies need Read Message History.
- Showing its class and role icons. They're its own emoji, which Discord counts as external.
- Mentioning the people or role a post is set to ping. @here, or a role nobody can mention, needs Mention Everyone.

It never reads your server's messages. It sees the slash commands and button presses sent to it. It looks up the
server's channels and roles, so officers can pick where it posts and who it pings, and the members it needs to match
Discord accounts to your roster: their nickname, roles and picture.

## Privacy

What the site and the bot keep is on the [privacy page](https://guildgolem.com/about/privacy).

## Problems and ideas

Open an [issue](../../issues) here and pick "Something's wrong" or "An idea", or use Feedback on any page of
[guildgolem.com](https://guildgolem.com).

## License

These docs are copyright 2026 Guild Golem (guildgolem.com) and shared under [CC BY 4.0](LICENSE). You may copy and change
them, in your own server or anywhere else, as long as you credit Guild Golem. The bot's code isn't public.
