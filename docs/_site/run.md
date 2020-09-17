# Run the TalentView apps locally

## Prerequisites

### Mongo

Run Mongo:

```
mongod --dbpath /usr/local/var/mongodb
```

### Mail catcher

With the mail catcher, you can view all the emails sent by the apps.

Install and run the mail catcher:

```
gem install mailcatcher
mailcatcher
```
It runs on port `1080` by default, you can view the emails sent by the app on [http://localhost:1080/](http://localhost:1080/){:target="_blank"}.


## API

View the gem list:
```
rvm gemset list
```
Install the gems:
```
gem install bundler
bundle install
```
Create the `application.yml` file inside `config/` and ask another developper for its content.

Create and populate the database:
```
rails db:create
rails db:migrate
rails db:seed
```

To run the API, you can either:
- Use the `rails command:
```
rails s -b 'ssl://api.talentview.dev:3000?key=config/ssl/server.key&cert=config/ssl/server.crt'
```
- Execute the `boot.sh` file (which contains the command above):
```
./boot.sh
```

In a second terminal, run the following command that handles slow processes of the API:
```
rails jobs:work
```

The API is now fully running. You can test webservices using Postman.

## Admin

Copy the `.env.example` file into a new `.env` file at the root of the project and ask another developper to provide you with the content:

```
API_URL=
AWS_S3_URL=
AWS_S3_BUCKET=
AWS_S3_REGION=
CAMERATAG_APPLICATION_UUID=
ENVIRONMENT=
FILESTACK_API_KEY=
FUNNEL_DOMAIN=
MANAGE_URL=
```

Make sure you are using the correct Node version (13.12.0) using nvm, then install the dependencies:
```
npm install
```
Run the app:
```
npm run dev
```

Go to [http://admin.talentview.test:4002]("https://admin.talentview.dev:4002"){:target="_blank"}.

## Manager and Funnel

The Manager and Funnel apps both run on the same version of Node (8.11.3), thus are run using the same commands.

Create a `.env.json` file at the root of the project and ask another developper for its content.

Make sure you are using the correct Node version using nvm, then install the dependencies:
```
npm install -g gulp
```
You might encounter an error caused by Xcode. If so, run command below then reinstall the dependencies:
```
sudo xcode-select --switch /Library/Developer/CommandLineTools
```
You might also encounter an error caused by `jspm`. If so, create a [token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token "link to tutorial"){:target="_blank"} on GitHub and use it instead of the password when running the following command:
```
jspm registry config github
```
Run the app:
```
gulp serve
```

Go to [https://manage.talentview.dev:4001]("https://manage.talentview.dev:4001"){:target="_blank"} and [https://talentview.talentview.dev.io:4000]("https://talentview.talentview.dev.io:4000/"){:target="_blank"}.

&nbsp;

# Congrats! You reached the end of the tutorial :)

&nbsp;

[Back: SSL certificates](./ssl.md)  |  [Return to index](./index.md)
