# QuickCord
An easy way to make discord bots!

## How to install?
```
npm i quickcord.js
```
## How to use?

Use the following code to use the library!
This library will be updated every so often!

### Starter code
```
const cli = require('quickcord.js');
var prefix = '!';
const pack = require('quickcord.js/package.json');
var dev = 'YOUR NAME';
// commands
cli.send('channel', `${prefix}help`, `${prefix}ping\n${prefix}about\n${prefix}dev\n${prefix}version`);
cli.status('WATCHING', 'The development of QuickCord!') // You can set WATCHING to -> PLAYING/LISTENING
cli.send(`reply`, `${prefix}ping`, `pong!`);
cli.send(`channel`, `${prefix}about`, `A discord bot created with an easy to use library to create a simple chat bot!`);
cli.send(`channel`, `${prefix}dev`, `My developer is: ${dev}`);
cli.send(`channel`, `${prefix}version`, `Current package version i am running on: ${pack.version}`);
cli.login('TOKEN');
```
#### Commands
cli.log('Hello world') 
Will display: QC -> Hello world

cli.login(token) 
Will display: QC -> Bot online! (Check discord if the bot is online!)

cli.send('channel', `${prefix}hi`, 'hello!');
Will display: hello! (In a discord channel where **${prefix}hi** was used)

cli.send('reply', `${prefix}hi`, 'hello!');
Will display: @user, hello! (In a discord channel where **${prefix}hi** was used)

cli.status('WATCHING', 'The development of QuickCord!')
Will display a user status of WATCHING, this can also be changed to: **WATCHING/LISTENING/PLAYING**, and then the content.

cli.embed(`#22e238`, `mb!help`, `Help Center`, `These are all the commands!`);
Will display:
```
Help Center

These are all the commands!
```

cli.inviteURL(`BOT-ID`, '8')
Will display: an invite link with admin perms.

### Events

cli.event.channelCreate(`Channel created: `);
Will display: Channel created: (Channel id) <- IN LOGS

cli.event.channelDelete(`Channel deleted: `);
Will display: Channel deleted: (Channel id) <- IN LOGS

### api

cli.api.ed_dbl(command, botid);
Will display: discord bot site embed

### DANGER
cli.kill(`OwnerID`);
This stop the **node.js** app.

#### Take note!
`Info` Please use the following as the qoute-tation marks for the grey boxes: `"# quickcord.js" 
