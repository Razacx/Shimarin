# Setup guide

## Requirements

- Node.js (8.9.3+) 
- NPM (5.5.1+)
- Typescript (2.7.2+)  
Install by running: `npm i -g typescript`

(These are the versions that were used during development, it may work perfectly fine on other versions)

- Discord Bot token
- Google Youtube API token

## Downloads
Clone the repository or [download it as a .zip file](https://github.com/Razacx/Shimarin/archive/master.zip)

## Setup

### Getting a Discord Bot token

1. Go to 
https://discordapp.com/developers/applications/me
2. Press 'New App' 
![](./img/discord-bot-token/new-app.PNG)
3. Set app name, description (optional) and icon (optional)  
Then press 'Create App'
![](./img/discord-bot-token/app-info.PNG)
4. Scroll down and click 'Create a Bot User'
![](./img/discord-bot-token/create-bot-user.PNG)
5. **Click 'click to reveal' to get your bot token. Keep this safe.**
![](./img/discord-bot-token/click-to-reveal.PNG)

### Getting a Google Youtube API token

1. Go to 
https://console.developers.google.com
2. Create a new project
3. In the dashboard, click 'Enable apis and services'
![](./img/google-api-token/enable-apis-and-services.PNG)
4. Pick 'Youtube Data API v3'
![](./img/google-api-token/pick-service.PNG)
5. Click 'Enable'
6. Go to 'Credentials' and create a new 'API key'
![](./img/google-api-token/create-api-key-credentials.PNG)
7. **Your new API key should be ready now.** 
8. (optional) Click 'Restrictions' -> 'API Restrictions' and select 'Youtube Data API v3'
![](./img/google-api-token/api-restrictions.PNG)

### Configuring Shimarin

Open `src/properties.ts` in your favourite text editor
![](./img/properties/properties.PNG)

Replace the parameters containing 'CHANGE THIS' with the following:

1. The text channel you want the bot to post messages in. Can be found by right-clicking the text channel and choosing 'Copy ID'.
2. Your Discord Bot token (see earlier in this document).
3. The id of the bot owner (you). Can be found by right-clicking your own name in discord and choosing 'Copy ID'.
4. Your Google Youtube API token (see earlier in this document).

All other bot properties have a brief description, configure them as you want.  
I wouldn't put any of the delays too low though, because you'll run into rate-limiting issues then.

### Downloading dependencies

Run this (from the root directory):
````
npm install
````

### Running Shimarin

#### Unix shell 
If you're using a unix-based shell, you can just run (from the root directory)   
This should build the typescript code and start the bot.  
````
npm start
````  


If you want to log the output to a file, you can instead run:  
````
npm start 2>&1 | tee -a ./log.txt
````

#### Windows

I currently haven't configured anything for running on windows.  
Executing the following commands should work though:

````
tsc
node ./target/app.js
````

**In the future I might provide simple binaries that you can just run normally**