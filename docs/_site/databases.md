# Databases

Two types of databases are used in **TalentView**:
- A SQL database for companies, users, campaigns, candidacies,...
- A NoSQL database for messages, comments,...

## PostgreSQL

Install PostgreSQL:
```
brew install postgresql
```
Also install the PostgreSQL [app](https://postgresapp.com/ "link to website"){:target="_blank"}.

## Mongo

Install Mongo:
```
brew tap mongodb/brew
brew install mongodb-community@4.4
```
View the services list:
```
brew services list
```
Start the service:
```
brew services start mongodb-community@4.4
```

&nbsp;

[Back: tools](./tools.md)  |  [Back to index](./index.md)  |  [Next: SSL certificates](./ssl.md)
