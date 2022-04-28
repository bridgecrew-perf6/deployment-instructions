### Prerequisits
---

1. Create a free Heroku account.
2. Install [Heroku CLI](https://cli.heroku.com/).

### Deployment
---

1. Make sure you have `engine` property defined inside your package json, it should match with your current version of node installed within your system.
  - to check current version of node, run this command inside you local machine: `node -v`, which will show `v16.14.0`
  - if its version is 16.x.x then write following inside `package.json`
    ```
    {
      ...
      "engines": {
        "node": "16.x"
      }
      ...
    }
    ```
2. Once this is done, you can directly start your app locally using following command
  `heroku local web`
3. Now create a `Procfile`, a file without any extension, which is required for deployment.
4. This file will have instructions for running your node app on deployment server.
   the content will look something like this: `web: node app.js`, make sure the file name matches with your starting point of node app.
5. Once done, commit your changes and push.
6. Now create heroku app using following command:
   `heroku create`
   This will create a app using your profile, which can be visited later via dashboard.
7. Now run following command:
   `git push heroku main`
8. To open deployed app run following command:
   `heroku open`
