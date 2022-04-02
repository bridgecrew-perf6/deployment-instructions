### `.env` setup
---

#### creating `.env` file

1. Create a `.env` file inside app's root folder.
2. Add required variables, this file may contain following contents:
   ```
   PORT=3000
   MONGODB_URL=URL_TO_MONGODB
   SERVER_URL=URL_TO_SERVER
   ```
   This file will have actual values, which are required for the app to be functional
3. Create a duplicate env file with name `.env.example`
4. In this file, do not put actual required env values, but keep the required keys with some dummy values as shown above
   This is done, if your project is open source, and you want community to understand what are the required variables to run this app.
5. Now add only `.env` inside `.gitignore` file, to exclude your actual env file.
   This is done to avoid any revelations of any classified information such as database location, private servers, etc.

#### utilizing `.env` file
1. Install dotenv package using follwoing command
   `npm i dotenv`
2. Once it is installed, import the package wherever required.
   `import dotenv from 'dotenv';` or `const dotenv = require('dotenv');`
3. Now call config method for dotenv:
   `dotenv.config();`
4. To get env values from env file, write following code:
   `process.env.{ENV_KEY}`
   For an instance you want to access `PORT` for your server
   `const PORT = process.env.PORT;`
5. Now check if everything is working as expected by running server locally.
6. If yes, commit the files, this time `.env` file will be excluded since we have added it in `.gitignore`.


### `.env` file setup in heroku
---
1. Once the project is deployed, open the app settings from dashboard.
2. Go to *Config vars* section and click on *reveal config vars* button.
3. Add environmental variables with their values as per your env file.


### `.env` file setup in vercel
---
1. Once the project is deployed, open the app settings from dashboard.
2. Go to *Environmental Variables* section 
3. Add environmental variables with their values as per your env file.
