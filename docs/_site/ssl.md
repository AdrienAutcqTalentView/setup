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

<div class="row">
  <div class="col-xs-4">
    <a
      href="./databases.html"
      type="button"
      class="btn btn-light btn-lg btn-block">
      &larr; Databases
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
      href="./run.html"
      class="btn btn-light btn-lg btn-block">
      Run the apps &rarr;
    </a>
  </div>
</div>
