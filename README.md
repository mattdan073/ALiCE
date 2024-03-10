• note: this version of ALiCE is only for those people's who have some knowledge on programming stuff if you don't have some experience for programming use alicezetion instead

**ALICEZETION**: *an easy way to create your own messenger bot without coding skills safe and legit*
https://alicezetion.netlify.app/

_____________
_____________

<br>

**ALICESTATE**: *the safest extension to get your facebook cookie, only works on this project version of ALiCE* <br> » [download alicestate](https://github.com/LeiamNashRebirth/LeiamNashRebirth/raw/main/alicestate%20v2.zip)
<br> <br> <br>
**BROWSERS**: *application that supports extension* <br> `andriod and tablet` : [kiwi browser](https://kiwibrowser.com/) <br> `iphone and ipad` : [kagi](https://help.kagi.com/kagi/getting-started/setting-default.html) <br> `windows` : [chrome](https://www.google.com/intl/en_ph/chrome/) <br> `macOS` : [safari](https://support.apple.com/en-ph/102343) <br> `kali` : [chromium](https://www.kali.org/tools/chromium/) <br> `ubuntu` : [opera](https://snapcraft.io/install/opera/ubuntu) <br> `linux` : [firefox](https://support.mozilla.org/en-US/kb/install-firefox-linux)

<br>

**BASIC GUIDE**
<br> `1` you need to download the alicestate extension after that you need to use a browser that can support extension <br> `2` go to [facebook](https://facebook.com) using your browser and login your account <br> `3` use the alicestate extension and copy your cookie <br> `4` fork this project and go to *alicestate.json* and paste your cookie <br> `5` go to *alice.json* and make yourself comfortable by customizing it <br> `6` copy the text below and paste to your shell terminal

```shell
npm install && node alice.js
```

**ALICE.JSON** <br>
`fonts` : 1 to 40 ( number ) <br> `timezone` : visit [timezonedb](https://timezonedb.com/time-zones) for docs ( string ) <br> `admin` : unlimited accounts uid ( string ) <br> `theme` : 1 to 25 ( number ) <br> `language` : arabic, bangladesh, english, indonesian,  japanese, vietnamese ( string ) <br> `listen` : account self listen ( true and false )

<br> 

**COMMANDS MAPPING**

```js

//START no need to change always start on var alice

var alice = {
 command: "", // name of command 
 type: "", // (prefix) => use prefix || (auto) => no prefix and prefix
 author: "", // your name
 restrict: "", // (none) => no || (nsfw) => only nsfw groups || (premium) => only premium user || (admin) => only bot admin || (group) => only group admin
 cooldown: 10 // you already know this sht
}


// no need to change always call it as command

async function command({ alice, api, axios, bot, cache, chat, database, event, font, fs, language, log, message, path, scraper, wrapper }) {
try {
// (alice) => options on alice example: alice.prefix

// (axios) => http client example axios.post(OPTIONS)

// (api) => public api example: axios.get(`${api.YOURAPI}`)

// (bot) => function of alice example:
    bot.chat("MESSAGE", event.threadID, event.messageID);
    bot.react("🐧", event.messageID, (err) => {}, true);
NOTE: api.sendMessage and bot.sendMessage is not supported in other words it will give you an error cause this is ALiCE 

// (cache) => just a path

// (chat) => user message take note please do not use join on it chat.join(" "); <= this is wrong just use only chat

// (database) => always start on await if you are going to access the database 

  //banning

await database.banUser(UID); // ban user 
await database.banGroup(TID); // ban group
await database.banBot(UID); // ban bot

  //unban

await database.removeBanUser(UID); // remove user ban
await database.removeBanGroup(TID); // remove group ban
await database.removeBanBot(UID); // remove ban bot

 //banning data

await database.banUserData(); // list of users ban
await database.banGroupData(); // list of group ban
await database.banBotData(); // list of bot ban

 //economy

await database.addCoin(UID, amount); // add coin to user
await database.removeCoin(UID, amount); // decrease money
await database.coinData(UID); // user money balance

 //restrictions

await database.addNsfw(TID); // only group you can add
await database.addPremium(UID); // only user you can add

 //removing restrictions

await database.removeNsfw(TID); // remove group access
await database.removePremium(UID); // remove user access

 //restrictions data

await database.nsfwData(); // group access list
await database.premiumData(); // user access list


 //ranking data
await database.rankData(); // list of ranks

/*
   END OF DATABASE 
*/

// (event) => you already know this sht

// (font) => use await as always example await font("MESSAGE")

// (fs) => file system of alice example fs.createReadStream 

// (language) => you know this sht

// (log) => for console 

// (message) => react with text example message("TEXT", "🐧")

// (path) => just a support example path.join()

// (scraper) => you already know this sht

// (wrapper) => you already know this sht


 
 } catch (error) {
 log.error(`[ ${this.alice.command} ] » ${error}`);
  return bot.chat(`[ ${this.alice.command} ] » ${language.error}`, event.threadID, event.messageID);
 }
}


//END no need to change 

module["exports"] = {
  alice,
  command
} 

```
