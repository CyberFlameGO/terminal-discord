# Terminal-Discord

![terminal-discord](https://image.ibb.co/gNnGsR/examplediscord.png)

A simple terminal based client for Discord using the [discord.js](https://discord.js.org) API.

## Installation
Clone the repository to a directory of your choice.
Find your token and add it to the config file.
Run sudo ./install.sh

## Config-File

### Token

Terminal-Discord uses a token to login rather than email and password since discord.js doesn't support that method anymore.
To retrieve your token open up your Discord client and press Ctrl-Shift-I. Navigate to the Application tab and find the token in the local storage.

![Token](https://image.ibb.co/iXBLK6/discord_token.png)

### MaxNameLength

The maximum length of usernames. If the value is null no extra spaces will be added to names and the messages will not be alligned

### Seperator

Seperator between username and message content.

### HistoryLength

Number of messages loaded at a time.

### defaultGuild

If not null this corresponds to the index of the guild you want selected at startup.

### defaultChannel
If not null this corresponds to the index of the channel you want selected at startup.

If the item is on the first page of the selection interface then the index is
*displayed\_number -1*

If the item is on another page then the index is
*displayed\_number -2 + (page\_number - 1) * 8*

### prompt
The prompt used.

### colorsupport
Wether color for usernames is enabled or not.

### mentionColor
What background color the message should have when you get mentioned. Only applicable when colorsupport is enabled. Setting this to null disables the feature.

### usenick
Wether the nickname should be displayed when available.

### time
Show the timestamp next to a message.

### date
Enable date support to display DD.MM.YYYY in front of the time.


## Commands

Enter a command while in a channel using /.

__q__ or __quit__: exits the client

__u__, __update__, __r__, __refresh__: refreshes manually

__nick__: changes your nickname

__d__, __delete__: deletes the last sent message

__e__, __edit__: replace the content of your last sent message with the string after /e

__m__, __menu__: open the channel selection menu to switch to a different channel

__o__, __online__: show a list of currently online users

__g__, __gr__, __group__: open group chat selection menu to switch to a different channel

__dm__, __pm__: open dm chat selection menu to switch to a different channel


Note that edit and delete only work on messages sent in the current session. If you haven't sent a message in the current session the command will do nothing.
