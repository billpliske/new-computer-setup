# new-computer-setup

## Mac

#### X-Code

- `xcode-select --install`

#### Homebrew

- `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- `brew update`
- `brew bundle dump` # creates a Brewfile - save that file and run brew bundle to install all of them at once

#### iTerm2

`brew cask install iterm2`

#### Bash

- `brew install bash # latest version of bash`

#### Git

- `brew install git`

#### Version control (which branch?)

- `brew install vcprompt`

#### NVM / Node

- `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash`
- `nvm install stable`
- `mkdir ~/workspace`
- `npm install -g lite-server eslint`
- `brew cask install visual-studio-code`

# Setting up new frontend projects

#### .eslintrc file

```javascript
{
  "extends": ["react-app", "prettier"],
  "plugins": ["prettier"],
  "rules": {
    "no-console": "off",
    "no-use-before-define": "off",
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 4
      }
    ]
  }
}
```

#### packages you need

```json

"eslintConfig": {
    "extends": "react-app"
  },

"devDependencies": {
    "eslint-config-prettier": "^6.10.1",
    "eslint-plugin-prettier": "^3.1.2",
    "prettier": "^2.0.2"
  }
```

#### vscode json

````json{
    ///////////////////////////////////
    // ESLINT KEY SETTINGS
    ///////////////////////////////////
    // tell the ESLint plugin to run on save
    "editor.codeActionsOnSave": {
        "source.fixAll": true
    },
    "editor.formatOnSave": true,
    "eslint.alwaysShowStatus": true,
    // turn it off for JS and JSX, we will do this via eslint
    "[javascript]": {
        "editor.formatOnSave": false
    },
    "[javascriptreact]": {
        "editor.formatOnSave": false
    },
    // Optional BUT IMPORTANT: If you have the prettier extension enabled for other languages like CSS and HTML, 
    turn it off for JS since we are doing it through Eslint already
    "prettier.disableLanguages": [
        "javascript",
        "javascriptreact"
    ],
    ///////////////////////////////////
    ///////////////////////////////////
    "editor.fontFamily": "Fira Code Regular",
    "editor.fontLigatures": true,
    "editor.fontSize": 18,
    "editor.minimap.enabled": false,
    "editor.renderControlCharacters": false,
    "editor.renderIndentGuides": false,
    "editor.snippetSuggestions": "top",
    "editor.tabSize": 4,
    "emmet.includeLanguages": {
        "javascript": "javascriptreact"
    },
    "emmet.syntaxProfiles": {
        "javascript": "javascriptreact"
    },
    "files.associations": {
        "*.js": "javascriptreact"
    },
    "files.autoSave": "onFocusChange",
    "files.trimTrailingWhitespace": true,
    "html.format.enable": true,
    "html.format.preserveNewLines": true,
    "javascript.updateImportsOnFileMove.enabled": "always",
    "javascript.validate.enable": false,
    "liveServer.settings.donotShowInfoMsg": true,
    "material-icon-theme.showUpdateMessage": false,
    "terminal.integrated.fontFamily": "Delugia Nerd Font",
    "terminal.integrated.fontSize": 17,
    "window.zoomLevel": 0,
    "workbench.colorTheme": "Atom One Dark",
    "workbench.editor.tabSizing": "shrink",
    "workbench.iconTheme": "material-icon-theme",
    "workbench.sideBar.location": "left",
}```
# install vscode extensions

#### bash_profile
````
