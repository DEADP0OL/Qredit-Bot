# DiscordBot API Scripts for Delegate and Voter Messages

A set of algorithms to analyze the Qredit blockchain and provide Discord messages.

## Notifications

- Missed Blocks
- Wallet Offline (In Development)
- Potential Fork in a Core Node (In Development)
- Network Consensus Below Threshold (In Development)

## Responses

- **delegate** ([*username*] or [*rank*]) - Provides information of a delegate. Defaults to rank 51.
- **rednodes** (*mainnet*) - Lists delegates that are currently missing blocks.
- **height** (*mainnet*) - Provides the current height accross mainnet or testnet nodes.

## Installation

Linux Ubuntu 16.10 and greater

```git clone https://github.com/DEADP0OL/Qredit-Bot```

```cd Qredit-Bot```

```sudo apt-get install python3-pip```

```sudo pip3 install setuptools```

```sudo pip3 install requests```

```sudo pip3 install pandas```

```sudo pip3 install packages```

```sudo pip3 install discord.py```

## Configuration

Copy default discord config.

```cp configs/default_discord.json configs/discord.json```

Edit the active config file.

```nano configs/discord.json```

- **apitoken**: The apitoken assigned to your bot
- **blockinterval**: The number of consecutive missed blocks required to reissue a notifications
- **minmissedblocks**: The number of consecutive missed blocks required for an initial notification
- **numdelegates**: The number of forging delegates on the blockchain
- **notificationmins**: The number of minutes to update delegate information for mainnet and testnet
- **commandprefix**: The character prefix for each bot function for the bot to listen for
- **bot_server**: The discord server to use for notifications and responses
- **listen_channels**: The discord server to use for notifications and responses
- **elevatedperms**: A list of permission groups to have full bot permissions
- **msglenlimit**: The character limit for messages on the discord server
- **priceurl**: The api url to obtain price data

## Activation

Start the python script.

```cd Qredit-Bot```

```python3 discordbot.py```

To keep the python script running after closing the terminal run the following command.

```nohup bash discordbot.sh &```

To end the python script run the following command.

```pkill -f discordbot```
