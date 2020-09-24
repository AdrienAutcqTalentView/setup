# Basic installs

## Apps to install

If you just received an out-of-the-box Mac, you need a few apps:

- Xcode (from AppStore)
- Google Chrome (as a suggested browser)
- Sublime Text (as a suggested IDE)

## Homebrew

Homebrew is MacOS' package manager. Install it by running:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

## IDE configuration

This section is useful only if you intend to use **Sublime Text** as your IDE.

First of all, you need to install the **Package Control** plugin. Then, type `CMD` + `SHIFT` + `P`, then `Package Control: Install Package` to open the package installation menu.

Here are the interesting packages to work with when on a **AngularJS** project:

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

### Postman (optional)

Postman is usefull to test the web services coming from the API. You can download it from [here]("https://www.postman.com/downloads/"){:target="_blank"}.

### Pimp your terminal (optional)

You can improve you terminal's colors and theme by using **Oh My Zsh**. Details [here](https://blog.edenpulse.com/boostez-votre-terminal-sous-osx/ "link to website"){:target="_blank"}.

### Team communication tools

At **TalentView**, we use the following communication tools:
- Slack
- Discord

&nbsp;

<div class="row">
  <div class="col-xs-6">
    <a
      href="./index.html"
      type="button"
      class="btn btn-light btn-lg btn-block">
      &larr; Return to index
    </a>
  </div>
  &nbsp;
  <div class="col-xs-6">
    <a
      href="./clone-repos.html"
      class="btn btn-light btn-lg btn-block">
      Cloning repositories &rarr;
    </a>
  </div>
</div>
