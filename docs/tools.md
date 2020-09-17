# Tools

## Node

Node allows to run JavaScript applications. It is used for the three **TalentView** clients.

### NVM

TalentVew's front apps use different **Node** versions. NVM (Node Version Manager) is useful to handle several versions on your machine. [Click](https://medium.com/@jamesauble/install-nvm-on-mac-with-brew-adb921fb92cc "link to website"){:target="_blank"} and install.

### Creating an environment variable

Create an environment variable to use the nvm command by pasting the following in your `~/.zshrc` file:
```
# Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$PATH:$HOME/.rvm/bin"
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion
source $(brew --prefix nvm)/nvm.sh
```
If the `~/.zshrc` file does not exist, create it.

### Node versions

Then, install the Node versions used at **TalentView**:
```
nvm install 13.12.0
nvm install 8.11.3
```
You can see the list of installed Node versions using:
```
nvm list
```
And set up your default Node version using:
```
nvm alias default 13.12.0
```
Finally, switch to another Node version with:
```
nvm use 13.12.0
```

## Ruby

Ruby is used for the API. Similarly to NVM, [RVM](https://rvm.io/rvm/install "Link to website"){:target="_blank"} is the Ruby Version Manager. Install it by running:

```
\curl -sSL https://get.rvm.io | bash -s stable
```
Install the Ruby version used in the API:
```
rvm install ruby-2.5.0
```
Use `rvm list` to access the list of installed Ruby versions and `rvm use` to switch between versions.

&nbsp;

<div class="row">
  <div class="col-xs-4">
    <a
      href="./clone-repos.html"
      type="button"
      class="btn btn-light btn-lg btn-block">
      &larr; Cloning repositories
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
      href="./databases.html"
      class="btn btn-light btn-lg btn-block">
      Databases &rarr;
    </a>
  </div>
</div>
