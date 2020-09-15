# Installs to run TalentView locally

## Apps to install

- Xcode (from AppStore)
- Google Chrome (as a suggested browser)
- Sublime Text (as a suggested IDE)

## IDE configuration

This section is useful only if you intend to use **Sublime Text** as your IDE.
First of all, you need to install the **Package Control** plugin. Then, type `CMD` + `SHIFT` + `P`, then `Package Control: Install Package` to open the package installation menu. Here are the interesting packages to work with when on a **AngularJS** project: 
>A File Icon, All complete, Angular CLI, AngularJS, AngularJS snippets, Babel, BracketHighlighter, ColorPicker, CSS3, DocBlockr, Emmet, Git, GitGutter, JSCS-Formatter, JSPrettier, MarkdownPreview, Material Theme, Sass, SCSS, Sidebar Enhancement, Stylus, SublimeLinter, SublimeREPL, Terminal, TrailingSpaces.

Finally, set up your configuration file to use the TalentView standard. Type `CMD` + `,` and paste the following on the user side:
```json
{
  "auto_complete": true,
  "auto_complete_commit_on_tab": true,
  "auto_complete_delay": 30,
  "bold_folder_labels": true,
  "color_scheme": "Packages/Material Theme/schemes/Material-Theme-Palenight.tmTheme",
  "draw_white_space": "all",
  "ensure_newline_at_eof_on_save": true,
  "folder_exclude_patterns":
  [
    "node_modules",
    "jspm_packages",
    "bower_components",
    ".git",
    ".sass-cache",
    ".tmp"
  ],
  "font_size": 12.0,
  "highlight_modified_tabs": true,
  "ignored_packages":
  [
    "Vintage"
  ],
    "rulers":
  [
    80
  ],
  "tab_size": 2,
  "theme": "Material-Theme.sublime-theme",
  "translate_tabs_to_spaces": true
}
```
## Others

### Pimp your terminal

You can improve you terminal's colors and themes by using **Oh My Zsh**. Details [here](https://blog.edenpulse.com/boostez-votre-terminal-sous-osx/ "link to website").

### Homebrew

Homebrew is MacOS' package manager. Install it by running:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
### Node version manager

TalentVew's front apps use different **Node** versions. NVM (Node Version Manager) is useful to switch versions. [Click](https://medium.com/@jamesauble/install-nvm-on-mac-with-brew-adb921fb92cc "link to website") to install.
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
### Ruby version manager

Similarly to NVM, [RVM](https://rvm.io/rvm/install "Link to website") is the Ruby Version Manager. Install it by running:
```
\curl -sSL https://get.rvm.io | bash -s stable
```
Install the Ruby version used in the API:
```
rvm install ruby-2.5.0
```
Use `rvm list` to access the list of installed Ruby versions and `rvm use` to switch between versions.

### PostgreSQL

Install PostgreSQL:
```
brew install postgresql
```
Also install the PostgreSQL [app](https://postgresapp.com/ "link to website").

### Mongo

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
