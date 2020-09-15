## Run the TalentView apps locally

### SSL certificates

In your `/etc/hosts` file, paste the following:
```
# TalentView
127.0.0.1 manage.talentview.dev
127.0.0.1 api.talentview.dev
127.0.0.1 admin.talentview.dev
127.0.0.1 http://talentview.talentview.dev.io/
```
Ask for the SSL config files to another developper. Save them on your machine, for example under `~/local-ssh`. Copy the `server.crt` and `server.key` in each corresponding repository root folder, except for the API, for which they go under `config/ssl/`.
Open the Trousseau d'accès -> Certificats, and place there the `rootCA.perm` files of each repository. Double-click on it -> Se fier -> Toujours approuver.

### Mongo

Run Mongo:
```
mongod --dbpath /usr/local/var/mongodb
```

### API

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
Install and run the mail catcher:
```
gem install mailcatcher
mailcatcher
```
It runs on port `1080`, you can view the emails sent by the app on [http://localhost:1080/](http://localhost:1080/).
To run the API, you can either:
- Use the rails command:
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

### Admin

Create a `.dev` file at the root of the project and ask another developper for its content.
Make sure you are using the correct Node version (using nvm), then install the dependencies:
```
npm install
```
Run the project:
```
npm run dev
```

### Manager and Funnel

Create a `.env.json` file at the root of the project and ask another developper for its content.
Make sure you are using the correct Node version (using nvm), then install the dependencies:
```
npm install -g gulp
```
You might encounter an error caused by Xcode. If so, run the following command:
```
sudo xcode-select --switch /Library/Developer/CommandLineTools
```
You might also encounter an error caused by `jspm`. If so, create a token on GitHub and use it instead of the password when running the following command:
```
jspm registry config github
```
Run the project:
```
gulp serve
```
