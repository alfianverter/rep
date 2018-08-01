# ***Tarkov Reputation Bot***
A Basic Bot for Tarkov Discords that has many features but not limited to being able to give and receive reputation. Run with discord.js on node. <br/>

There is very minimal commenting so have fun if you want to change things. Removing commands should be obvious however. <br/>

*If you are using this on a large server please put my github repo link somewhere*

***REMEMBER TO CHANGE THE PREFIX AND TOKEN IN THE CONFIG.JSON FILE***

# Installation
Project requires node and npm <br />
[Node Download Page](https://nodejs.org/en/download/)  Direct: [WINDOWS](https://nodejs.org/dist/v8.9.4/node-v8.9.4-x64.msi), [MAC](https://nodejs.org/dist/v8.9.4/node-v8.9.4.pkg) <br/>
 *node -v* Checks Node Version (requires 8.0 or later) <br/> *npm -v* Checks npm version <br/>

Step 1: Clone or Download Bot, unzip if you download it <br />
Step 2: Update ```config.json``` for your token and prefix <br />
Step 3: cd into file directory <br />
Step 4: ```npm install``` <br />
Step 5: ```node bot``` <br />

**If you get an error related to a file not existing, create a file reputation.json containing just '{}' <br/>**

# Required Roles CASE SENSITIVE

1. __Needed to use staff commands__
  - staff
2. __Needed to use shop commands__
  - trusted
3. __Recommended but Not Needed for other commands__
  - BEAR
  - USEC
  - Member (given with member)
  - notify (give on join or with notify)

# Commands List
All commands use the prefix + command style, prefix being defined in the ```config.json``` file


**Reputation Related Commands**

Command | Definition | Usage
------- | ------- | --------
(+/-)rep [username] | Give someone positive or negative reputation | +rep @cranberriez **Gives 1 positive rep**<br /> rep @cranberriez **Gives 1 positive rep**<br /> -rep @cranberriez **Gives 1 negative rep**
profile [username] (optional) | Shows the profile or positve and negative reputation of someone or yourself | profile **Shows your profile**<br /> profile @cranberriez **Shows cranberriez profile**
addshop [url] | Adds a shop url for yourself, only works for users with the **trusted_trader** role | addshop i.imgur.com **Adds any url as your shop**
shop [username] | Shows a trusted's shop | shop @cranberriez **Returns the url the trusted_trader set as their shop**
leaderboard | Shows top 3 users and their reputation <br /> Ignored users has to be hardcoded| leaderboard **Returns leaderboard**


**Miscellaneous Commands**

Command | Definition
------- | ----------
dice | Rolls a dice
coinflip | Flips a coin
member | Gives you the Member role
bear | Gives you the BEAR role
usec | Gives you the USEC role
notify | Gives you the notify role <br /> we use this to mention users that want news or info instead of doing @everyone
ping | pings the bot and shows latency
tarvu | Praise tarvu


**Raffle Commands**
<br />Note that raffles are per bot and not per server so they can be buggy

Command | Definition | Usage
------- | ------- | --------
raffle [max # of participants] | Starts a raffle that ends when specified number of people enter | raffle 3 **Starts a raffle that ends when 3 people enter**
enter | Enters ongoing raffle
participants | Lists all participants of current raffle

**Admin Commands**

Command | Definition | Usage
------- | ------- | --------
setrep | Gives or Removes, depending on +/-, another players' positive/negative reputation | setrep + @cranberriez 13 **Sets postive rep to 13**<br /> setrep - @cranberriez 12 **Sets negative rep to 12**
stopraffle | Stops current raffle
timedroles | Gives out roles based on time in the server | This is kinda complicated and unused by default, explanation below

# Timed Roles UNUSED
**Upon running the timedroles command, roles will be given out to everyone on the server according to their playtime stated below. Roles will be checked and re-given every day** Players who join the server for the first time WON'T be given the Hobo role, *this can be changed* <br /> <br />
Roles are CASE SENSITIVE to whatever they are in the bot.js file, you can change them but what is listed below are defaults.
- Hobo | *On Join*
- Newbie | *7 Days*
- Scav | *30 Days*
- Private | *2 Months*
- Captain | *4 Months*
- VETERAN | *6 Months*

# Amazon Setup
**We will be using AWS ec2 instances under the free tier. If this is the only bot running you shouldn't go past 750 hour limit per month, average month has 730 hours.**
