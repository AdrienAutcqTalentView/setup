# SSL certificates

Since the **TalentView** frontend apps use the `https` protocol, you need *SSL certificates* on your machine.

In your `/etc/hosts` file, paste the following:
```
# TalentView
127.0.0.1 manage.talentview.dev
127.0.0.1 api.talentview.dev
127.0.0.1 admin.talentview.dev
127.0.0.1 talentview.talentview.dev.io
```

Note you need to use `sudo vi`.
Ask another developper for the SSL config files. Save them on your machine, for example under `~/local-ssl`.

Copy the `server.crt` and `server.key` files in each corresponding repository root folder, except for the API, for which they go under `config/ssl/`.

Open the **Keychain Access** app &rarr; *Certificates*, and place there the `rootCA.perm` files of each project. Double-click on each certificate file. Under *Trust*, *When using this certificate* &rarr; *Always trust*. Fill in your session password every time it is required.

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
