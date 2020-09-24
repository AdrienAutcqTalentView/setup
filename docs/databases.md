# Databases

Two types of databases are used in the **TalentView** apps:
- A *SQL* database for entities with well defined data, such as: companies, users, campaigns, candidacies,...
- A *NoSQL* database for other entities: messages, comments,...

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

<div class="row">
  <div class="col-xs-4">
    <a
      href="./tools.html"
      type="button"
      class="btn btn-light btn-lg btn-block">
      &larr; Tools
    </a>
  </div>
  &nbsp;
  <div class="col-xs-4">
    <a
      href="./index.html"
      type="button"
      class="btn btn-light btn-lg btn-block">
      Return to index
    </a>
  </div>
  &nbsp;
  <div class="col-xs-4">
    <a
      href="./ssl.html"
      class="btn btn-light btn-lg btn-block">
      SSL certificates &rarr;
    </a>
  </div>
</div>
