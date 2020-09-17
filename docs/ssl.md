# SSL certificates

In your `/etc/hosts` file, paste the following:
```
# TalentView
127.0.0.1 manage.talentview.dev
127.0.0.1 api.talentview.dev
127.0.0.1 admin.talentview.dev
127.0.0.1 http://talentview.talentview.dev.io/
```
Ask for the SSL config files to another developper. Save them on your machine, for example under `~/local-ssh`.

Copy the `server.crt` and `server.key` files in each corresponding repository root folder, except for the API, for which they go under `config/ssl/`.

Open the **Keychain Access** app &rarr; *My Certificates*, and place there the `rootCA.perm` files of each repository. Double-click on each certificate file &rarr; *Trust* &rarr; *Always trust*. Fill in your session password every time it is required.

&nbsp;

[Back: databases](./databases.md)  |  [Back to index](./index.md)  |  [Next: run the apps](./run.md)
