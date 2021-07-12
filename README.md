# mogiri

Conference reception bot for Discord with connpass

## About

## Installation

**Node.js 14.0.0 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Please put these environment values on .env file on root dir.

```config/{development|production}.json
{
  "discord": {
    "privateKey": "Bot TOKEN for your Application in Discord DEVELOPER PORTAL",
    "roleForValidUser": "Name of the role to add to the userrole name",
    "observation": [
      "Chennel name to be observed"
    ]
  },
  "googlespreadsheet": {
    "sheetid": "Sheet ID from Google spreadsheet shared URL",
    "sheetname": "sheet name in spreadsheet",
    "orderrange": {
      "description": "Column range with the reception number.",
      "startRowIndex": 0,
      "endRowIndex": 500,
      "startColumnIndex": 0,
      "endColumnIndex": 0
    },
    "acceptrange": {
      "description": "Column range to enter the ID of the registered discord.(For more than two columns, make sure it works.)",
      "startRowIndex": 0,
      "endRowIndex": 500,
      "startColumnIndex": 1,
      "endColumnIndex": 1
    },
    "credentials": {
      "type": "ex. service account",
      "project_id": "youre project id",
      "private_key_id": "1234567890abcdef1234567890abcdef12345678"
    }
```



To register your bot to your server, please see...

Setting up a bot application : <https://discordjs.guide/preparations/setting-up-a-bot-application.html>

Adding your bot to servers : <https://discordjs.guide/preparations/adding-your-bot-to-servers.html>

## config and run

in bash

```
$ export NODE_ENV=production
$ node index.js
```

in Powershell

```
PS > $env:NODE_ENV=production
PS > node index.js
```

## Quick Example

```Shell
You> 大島さん
Bot> 児島だよ
 
You> My order number is 1234567
Bot> @You, XXXのロールをつけました！
```
