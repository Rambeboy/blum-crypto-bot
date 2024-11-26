# BLUM CRYPTO BOT

![blum](assets/img1.png)

Blum is telegram web app mining on telegram, and blum bot is blum auto mining and complete missions bot.

### REGISTER BLUM ACCOUNTS

- [Register Blum on telegram](https://t.me/blum/app?startapp=ref_LlFGpzHIGi)
- Start bot `/start`
- Launch Blum

## PREREQUISITE

- Node JS (v22.1.0)
- Git
- TELEGRAM_APP_ID & TELEGRAM_APP_HASH Get it from [Here](https://my.telegram.org/auth?to=apps)

## BOT FEATURE

- Auto Check In (Experimental)
- Auto start and claim mining
- Auto complete missions
- Auto claim misisons reward
- Auto play game

## SETUP & CONFIGURE BOT

### LINUX & MAC OS

1. Clone project repository
   ```
   git clone https://github.com/Rambeboy/blum-crypto-bot.git && cd blum-crypto-bot
   ```

2. Install dependencies
   ```
   npm install
   ```
   
3. Make new accounts folder
   ```
   mkdir -p accounts
   ```

4. Copy all folder
   ```
   cp config/config_tmp.js config/config.js && cp config/proxy_list_tmp.js config/proxy_list.js
   ```

5. Configure the config
   ```
   nano config/config.js
   ```
   And add your telegram app id and hash there (if you use telegram sessions).

6. Configure the proxy
   ```
   nano config/proxy_list.js
   ```
   And fill up your proxy using provided format (it currently support only HTTPS proxy), if you don't use proxy then just let it blank [].

   ```
   export const proxyList = [];
   ```

8. To start the app run
   ```
   npm run start
   ```

### WINDOWS

1. Open your `Command Prompt` or `Power Shell`.
2. Clone project repository
   ```
   git clone https://github.com/Rambeboy/blum-crypto-bot.git && cd blum-crypto-bot
   ```
3. Install dependencies
   ```
   npm Install
   ```
4. Navigate to `blum-crypto-bot` directory.
5. Make new folder named `accounts`.
6. Navigate to config folder and rename `config_tmp.js` to `config.js`, `proxy_list_tmp.js` to `proxy_list.js`.
7. Open and configure `config.js` and `pxoxy_list.js`.
8. Back to the `blum-crypto-bot` folder.
9. To start the app open your `Command Prompt` or `Power Shell` again and run.
    
   ```
   npm run start
   ```

## SETUP ACCOUNTS

1. Run bot `npm run start`.
2. Choose option `1` to create account.
3. Choose account type `Query` or `Sessions`
4. `Session` Type
- Enter Account Name.
- Enter your phone number starting with. countrycode ex : `+628xxxxxxxx`
- You will be asked for verification code and password (if any).
- Start The bot Again after account creation complete.
5. `Query` Type
- Enter Account Name
- Enter Telegram Query (you can get query by opening bot app on browser > inspect element > storage / application > session storage > telegram init params > copy tg web app data value).
- Start The bot Again after account creation complete.
6. After bot started choose option `3` start bot.
7.  if something wrong with your Account, reset Account (option 2) first or just delete problematic a, to cancel running bot press `ctrl+c` twice, and start again [from No 1.](#setup-accounts)
   

## SESSION TROUBLESHOOT
If you asked to enter phone number again after sessions creation, it mean session not initialized correctly, try to delete the created sessions. 

Example Case
- example you already have 1 session (sessionA) and all good when you run bot. After that you create another session, but when you run bot, the bot asked to enter phone number again, so the problem is on (sessionB), to fix it just remove the `accounts/sessionB` folder and re create it or just delete all folder inside `accounts` directory with prefix `sessions-`.

## QUERY TROUBLESHOOT
if your bot get eror, with some error code `401` it mean your query expired, go get new query and run bot again and choose option `4` for query modification. 

## HOW TO UPDATE

To update bot follow this step :
1. Run
   ```
   git pull
   ```
   or
   ```
   git pull --rebase
   ```
   if error run 
   ```
   git stash && git pull
   ```
2. Run
   ```
   npm update
   ```
3. Read Setup and run again if any new step added.
4. Run the bot again
   ```
   npm run start
   ```

## NOTE

Don't use bot with `session` type if you using telegram account that bought from someone because it can make your telegram account deleted. instead of using `session` type, use `query` type.

This bot can use Telegram Query and Telegram Sessions. if you want to use sessions, and ever use one of my bot that use telegram sessions, you can just copy the sessions folder to this bot. Also for the telegram APP ID and Hash you can use it on another bot. If you want to use Telegram Query, get your query manually.

If you got error `Invalid ConstructorId` try to run this ```npm i telegram@2.22.2```

## LICENSE

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
