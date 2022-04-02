### `.env` setup
---

1. create a `.env` file inside node app's root folder.
2. add required variables suce as following:
   ```
   PORT=3000
   MONGODB_URL=URL_TO_MONGODB
   ```
   Here this file will have actual values, which are required app to be functional
3. create a duplicate env file with name `.env.example`
4. Do not put actual required env values, but keep the required keys with some dummy values as shown above
5. Now add only `.env` inside `.gitignore` file, to exclude your actual env file.
   This is done to avoid any revelations of classified information such as database location, private servers, etc.
6. Now check if all is working as expected by running server locally.
7. If yes commit the files, this time `.env` file will be excluded since we have added it in `.gitignore`.

### `.env` file setup in heroku
---
1. Once the project is deployed, open the app settings from dashboard.
2. Go to Config vars section and click on *reveal config vars* button.
3. Add environmental variables with their values as per your env file.
