# My VSCode setup

## 1. Featured extension list:

### 📦 🤌 (Recommend) **TabOut** (albert.TabOut):

> 💅: This extension is very handy, you can use tab to get
> out bracket or quotes.

> 👎: Sometimes, it can conflict with intellisense.

**Keyboard shortcut:** `Tab`

---

### 📦 **Auto Add Brackets in String Interpolation** (aliariff.auto-add-brackets):

> 👎: Doesn't work with multiline template string.

---

### 📦 **statusbar-commands** (anweber.statusbar-commands):

> 💅: My favorite extension, I don't have to combine keybindings
> `Ctrl+Shift+P` to execute commands.

> 👎: Icon and text is not center aligned.

**Demo:**

![statusbar-command-demo](/assets/statusbar-command-demo.png)

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "statusbar_command.commands": [
    // To zoom font fast, I enable settings:
    // {"editor.mouseWheelZoom": true,}
    // but to reset font zoom is not easy.
    {
      "alignment": "left",
      "color": "#EA6962",
      "command": "editor.action.fontZoomReset",
      "id": "reset-zoom",
      "name": "Reset Font Zoom",
      "priority": -1,
      "text": "$(debug-restart)",
      "tooltip": "Resest font zoom"
    },
    // Quickly open settings.json file.
    {
      "alignment": "left",
      "color": "#E78A4E",
      "command": "workbench.action.openSettingsJson",
      "id": "open-settings",
      "name": "Open settings.json",
      "priority": -2,
      "text": "$(gear)",
      "tooltip": "Open settings.json"
    },
    // From update 1.61, you can split editor in group.
    {
      "alignment": "left",
      "color": "#D8A657",
      "command": "workbench.action.toggleSplitEditorInGroup",
      "id": "split-group",
      "name": "Split (Group)",
      "priority": -3,
      "text": "$(split-horizontal)",
      "tooltip": "Split an editor without creating a new group"
    },
    // Center editor window, I found it quite handy because I use thin cursor, it hard to track cursor.
    {
      "alignment": "left",
      "color": "#A9B665",
      "command": "center-editor-window.center",
      "id": "better-align",
      "name": "Center Editor Window (Extension)",
      "priority": -4,
      "text": "$(fold)",
      "tooltip": "Centers your editor window at the current cursor position"
    },
    // Sort JS object keys
    {
      "alignment": "left",
      "color": "#89B482",
      "command": "sortJsObjectKeys.sortJsObjectKeys",
      "id": "sort-object-keys",
      "name": "Sort JS object keys (Extension)",
      "priority": -5,
      "text": "$(arrow-down)",
      "tooltip": "Sort JS object keys (ascending)"
    },
    // Rarely use.
    {
      "alignment": "left",
      "color": "#7DAEA3",
      "command": "extension.changeCase.commands",
      "id": "change-case",
      "name": "Change Case (Extension)",
      "priority": -6,
      "text": "$(case-sensitive)",
      "tooltip": "Quickly change the case of the current selection or current word"
    },
    // Don't have to manually remove HTML tag.
    {
      "alignment": "left",
      "color": "#EA6962",
      "command": "editor.emmet.action.removeTag",
      "id": "remove-tag",
      "name": "Remove Tag (Emmet)",
      "priority": -7,
      "text": "$(trash)",
      "tooltip": "Remove HTML tag"
    },
    // Wrap selection with HTML tag.
    {
      "alignment": "left",
      "color": "#D8A657",
      "command": "extension.htmlTagWrap",
      "filterLanguageId": "html|javascriptreact",
      "id": "htmlwrap",
      "name": "HTML Tag Wrap (Extension)",
      "priority": -8,
      "text": "$(tag)",
      "tooltip": "Wraps selection in HTML tags"
    }
  ]
}
```

</details>

---

### 📦 **Docs View** (bierner.docs-view):

**Demo:**

![docs-view-demo](/assets/docs-view-demo.png)

From update [1.64](https://code.visualstudio.com/updates/v1_64#_new-side-panel), you can drag it to side panel for better view.

![docs-view-side-panel-demo](/assets/docs-view-side-panel-demo.png)

Or move it to panel view.

![docs-view-panel-demo](/assets/docs-view-panel-demo.png)

---

### 📦 🤌 (Recommend) **Print It** (bmalehorn.print-it):

**Keyboard shortcut:** `Alt+[`

---

### 📦 🤌 (Recommend) **htmltagwrap** (bradgashler.htmltagwrap):

> 👎: Need extra configurations to fix conflict with "Indent one space"
> extension.
>
> ```json
> { "indentOneSpace.onlyCompleteRange": true }
> ```

**Settings:**

<details>
<summary>settings.json</summary>

```json
{ "htmltagwrap.tag": "div" }
```

</details>

<details>
<summary>keybindings.json</summary>

```json
[
  {
    "key": "alt+/",
    "command": "extension.htmlTagWrap",
    "when": "editorTextFocus"
  },
  // Remove default keybindings
  {
    "key": "alt+w",
    "command": "-extension.htmlTagWrap",
    "when": "editorTextFocus"
  }
]
```

</details>

**Keyboard shortcut:** `Alt+/`

---

### 📦 🤌 (Recommend) **Bracket Select** (chunsen.bracket-select):

> 💅: I use it frequently, very very handy extension.

> 👎: Undo select conflict with GeForce Experience 🤷‍♂️.

**Keyboard shortcut:**

- Select inside bracket: `Alt+A`.
- Undo select bracket: `Alt+Z`.
- Select include bracket: `Ctrl+Alt+A`.

---

### 📦 **GitLens — Git supercharged** (eamodio.gitlens):

---

### 📦 **HTML CSS Support** (ecmel.vscode-html-css):

---

### 📦 🤌 (Recommend) **Prettier** (esbenp.prettier-vscode):

**Keyboard shortcut:** `Shift+Alt+F`

---

### 📦 **Auto Rename Tag** (formulahendry.auto-rename-tag):

> 💅: VSCode built-in setting: "editor.linkedEditing" isn't good enough.

---

### 📦 **Dummy Text Generator** (gurayyarar.dummytextgenerator):

---

### 📦 **Toggler** (hideoo.toggler):

**Settings:**

<details>
<summary>keybindings.json</summary>

```json
[
  {
    "key": "alt+\\",
    "command": "extension.toggle",
    "when": "editorTextFocus"
  },
  // Remove default keybindings
  {
    "key": "alt+r",
    "command": "-extension.toggle",
    "when": "editorTextFocus"
  }
]
```

</details>

**Keyboard shortcut:** `Alt+\`

---

### 📦 **Center Editor Window** (kaiwood.center-editor-window):

**Keyboard shortcut:** `Ctrl+L`

---

### 📦 **Image preview** (kisstkondoros.vscode-gutter-preview):

**Demo:**

![image-preview-demo](/assets/image-preview-demo.png)

---

### 📦 **Fluent Icons** (miguelsolorio.fluent-icons):

---

### 📦 **dotENV** (mikestead.dotenv):

---

### 📦 **Code Time** (softwaredotcom.swdc-vscode):

---

### 📦 🤌 (Recommend) **Rewrap** (stkb.rewrap):

> 💅: Wrap long comment, highly recommend.

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "rewrap.autoWrap.enabled": true,
  "rewrap.autoWrap.notification": "text",
  "rewrap.wrappingColumn": 80
}
```

</details>

---

### 📦 🤌 (Recommend) **Code Spell Checker** (streetsidesoftware.code-spell-checker):

---

### 📦 🤌 (Recommend) **Vietnamese - Code Spell Checker** (streetsidesoftware.code-spell-checker-vietnamese):

---

### 📦 **vscode-pdf** (tomoki1207.pdf):

---

### 📦 🤌 (Recommend) **Error Lens** (usernamehw.errorlens):

---

### 📦 **Indent one space** (usernamehw.indent-one-space):

**Settings:**

<details>
<summary>settings.json</summary>

```json
{ "indentOneSpace.onlyCompleteRange": true }
```

</details>

**Keyboard shortcut:**

- Indent one space: `Space`
- Reverse indent one space: `Shift+Space`

---

### 📦 🤌 (Recommend) **Highlight Matching Tag** (vincaslt.highlight-matching-tag):

**Demo:**

![highlight-matching-tag-demo](/assets/highlight-matching-tag-demo.png)

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "highlight-matching-tag.highlightSelfClosing": true,
  "highlight-matching-tag.showPath": false
}
```

</details>

---

### 📦 **WindiCSS IntelliSense** (voorjaar.windicss-intellisense):

> 💅: Many cool features from WindiCSS:
>
> - Autocomplete
> - Hover Preview
> - Syntax Highlighting
> - Color Preview
> - Code Folding
> - Compile Commands
> - Visual Analyzer
> - Sort class: I install package: `prettier-plugin-tailwindcss` instead, because not everyone use this
>   extension 🤷‍♂️.

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "windicss.enableCodeFolding": true,
  // "windicss.foldCount": 10,
  "windicss.foldByLength": true,
  "windicss.foldLength": 80
}
```

</details>

---

### 📦 🤌 (Recommend) **vscode-icons** (vscode-icons-team.vscode-icons):

---

### 📦 🤌 (Recommend) **TODO Highlight** (wayou.vscode-todo-highlight):

**Demo:**

![todo-highlight-demo](/assets/todo-highlight-demo.png)

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "todohighlight.defaultStyle": {
    "backgroundColor": "#7DAEA3",
    "before": {
      "contentText": "",
      "fontStyle": "normal"
    },
    "border": "1px solid #A9B665",
    "borderRadius": "5px",
    "color": "black",
    "cursor": "pointer",
    "isWholeLine": false,
    "overviewRulerColor": "#7DAEA3"
  },
  "todohighlight.exclude": [
    "**/node_modules/**",
    "**/bower_components/**",
    "**/dist/**",
    "**/build/**",
    "**/.vscode/**",
    "**/.github/**",
    "**/_output/**",
    "**/*.min.*",
    "**/*.map",
    "**/.next/**"
  ],
  "todohighlight.include": [
    "**/*.js",
    "**/*.jsx",
    "**/*.ts",
    "**/*.tsx",
    "**/*.html",
    "**/*.php",
    "**/*.css",
    "**/*.scss"
  ],
  "todohighlight.isCaseSensitive": true,
  "todohighlight.isEnable": true,
  "todohighlight.keywords": [
    "WORKING:",
    {
      "backgroundColor": "#E78A4E",
      "color": "black",
      "overviewRulerColor": "#E78A4E",
      "text": "BUG:"
    },
    {
      "backgroundColor": "#A9B665",
      "color": "black",
      "overviewRulerColor": "#A9B665",
      "text": "DONE:"
    },
    {
      "backgroundColor": "#D8A657",
      "color": "black",
      "overviewRulerColor": "#D8A657",
      "text": "NOTE:"
    },
    {
      "backgroundColor": "#EA6962",
      "color": "black",
      "overviewRulerColor": "#EA6962",
      "text": "TODO:"
    }
  ]
}
```

</details>

---

### 📦 **change-case** (wmaurer.change-case):

---

### 📦 🤌 (Recommend) **Local History** (xyz.local-history):

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "local-history.dateLocale": "vi-VN",
  "local-history.daysLimit": 1,
  "local-history.maxDisplay": 10,
  "local-history.saveDelay": 600
}
```

</details>

---

### 📦 **Sort JS object keys** (zengxingxin.sort-js-object-keys):

---

### 📦 🤌 (Recommend) **Bracketeer** (pustelto.bracketeer):

> 💅: Highly recommend.

> 👎: Sometimes it doesn't work.

**Settings:**

<details>
<summary>keybindings.json</summary>

```json
[
  {
    "key": "alt+'",
    "command": "bracketeer.swapQuotes"
  },
  {
    "key": "ctrl+shift+alt+;",
    "command": "-bracketeer.swapQuotes"
  },
  {
    "key": "alt+;",
    "command": "bracketeer.swapBrackets"
  },
  {
    "key": "ctrl+shift+alt+k",
    "command": "-bracketeer.swapBrackets"
  },
  {
    "key": "shift+alt+;",
    "command": "bracketeer.removeBrackets"
  },
  {
    "key": "ctrl+shift+alt+i",
    "command": "-bracketeer.removeBrackets"
  },
  {
    "key": "shift+alt+'",
    "command": "bracketeer.removeQuotes"
  },
  {
    "key": "ctrl+shift+alt+'",
    "command": "-bracketeer.removeQuotes"
  }
]
```

</details>

**Keyboard shortcut:**

- `Alt+'`: Swap quotes.
- `Alt+;`: Swap brackets.
- `Shift+Alt+'`: Remove quotes.
- `Shift+Alt+;`: Remove brackets.

---

### 📦 🤌 (Recommend) **Color Highlight** (naumovs.color-highlight):

**Demo:**

![color-highlight-demo](/assets/color-highlight-demo.png)

---

### 📦 🤌 (Super Recommend) **Gruvbox Material** (sainnhe.gruvbox-material):

---

### 📦 **Incrementor** (nmsmith89.incrementor):

> 💅: Highly recommend.

> 👎: You have to select the whole number to increase.

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "incrementor.enums.values": [
    ["false", "true"],
    ["let", "const"],
    ["public", "private", "protected"],
    ["top", "bottom"],
    ["left", "right"],
    ["relative", "absolute"],
    ["true", "false"],
    ["flex-start", "flex-end", "center"]
  ]
}
```

</details>

<details>
<summary>keybindings.json</summary>

```json
[
  {
    "key": "ctrl+;",
    "command": "incrementor.decrementByOne"
  },
  {
    "key": "ctrl+down",
    "command": "-incrementor.decrementByOne"
  },
  {
    "key": "ctrl+'",
    "command": "incrementor.incrementByOne"
  },
  {
    "key": "ctrl+up",
    "command": "-incrementor.incrementByOne"
  },
  {
    "key": "ctrl+alt+;",
    "command": "incrementor.decrementByTen"
  },
  {
    "key": "ctrl+shift+down",
    "command": "-incrementor.decrementByTen"
  },
  {
    "key": "ctrl+alt+'",
    "command": "incrementor.incrementByTen"
  },
  {
    "key": "ctrl+shift+up",
    "command": "-incrementor.incrementByTen"
  },
  {
    "key": "ctrl+shift+alt+;",
    "command": "incrementor.decrementByTenth"
  },
  {
    "key": "ctrl+shift+alt+down",
    "command": "-incrementor.decrementByTenth"
  },
  {
    "key": "ctrl+shift+alt+'",
    "command": "incrementor.incrementByTenth"
  },
  {
    "key": "ctrl+shift+alt+up",
    "command": "-incrementor.incrementByTenth"
  }
]
```

</details>

**Keyboard shortcut:**

- `Ctrl+'`: Increase by 1.
- `Ctrl+;`: Decrease by 1.
- `Ctrl+Alt+'`: Increase by 10.
- `Ctrl+Alt+;`: Decrease by 10.
- `Ctrl+Shift+Alt+'`: Increase by 0.1.
- `Ctrl+Shift+Alt+;`: Decrease by 0.1.

---

### 📦 🤌 (Recommend) **Subword Navigation** (ow.vscode-subword-navigation):

**Keyboard shortcut:**

- `Alt+➡️`: Cursor Subword Right
- `Shift+Alt+➡️`: Cursor Subword Right Select
- `Alt+⬅️`: Cursor Subword Left
- `Shift+Alt+⬅️`: Cursor Subword Left Select
- `Alt+Backspace`: Delete Subword Left
- `Alt+Delete`: Delete Subword Right

## 2. All extensions:

> You can use the command below to install all extensions 👇.

<details>
<summary>Extension list</summary>

```bash
code --install-extension albert.TabOut
code --install-extension aliariff.auto-add-brackets
code --install-extension anweber.statusbar-commands
code --install-extension bierner.docs-view
code --install-extension bmalehorn.print-it
code --install-extension bradgashler.htmltagwrap
code --install-extension chunsen.bracket-select
code --install-extension eamodio.gitlens
code --install-extension ecmel.vscode-html-css
code --install-extension esbenp.prettier-vscode
code --install-extension formulahendry.auto-rename-tag
code --install-extension gurayyarar.dummytextgenerator
code --install-extension hideoo.toggler
code --install-extension kaiwood.center-editor-window
code --install-extension kisstkondoros.vscode-gutter-preview
code --install-extension miguelsolorio.fluent-icons
code --install-extension mikestead.dotenv
code --install-extension mongodb.mongodb-vscode
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-toolsai.jupyter
code --install-extension ms-toolsai.jupyter-keymap
code --install-extension ms-toolsai.jupyter-renderers
code --install-extension ms-vscode.cpptools
code --install-extension ms-vsliveshare.vsliveshare
code --install-extension natqe.reload
code --install-extension naumovs.color-highlight
code --install-extension nmsmith89.incrementor
code --install-extension ow.vscode-subword-navigation
code --install-extension patbenatar.advanced-new-file
code --install-extension pflannery.vscode-versionlens
code --install-extension pustelto.bracketeer
code --install-extension ritwickdey.live-sass
code --install-extension ritwickdey.LiveServer
code --install-extension sainnhe.gruvbox-material
code --install-extension sburg.vscode-javascript-booster
code --install-extension softwaredotcom.swdc-vscode
code --install-extension stkb.rewrap
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension streetsidesoftware.code-spell-checker-vietnamese
code --install-extension tomoki1207.pdf
code --install-extension usernamehw.errorlens
code --install-extension usernamehw.indent-one-space
code --install-extension vincaslt.highlight-matching-tag
code --install-extension voorjaar.windicss-intellisense
code --install-extension vscode-icons-team.vscode-icons
code --install-extension wayou.vscode-todo-highlight
code --install-extension wmaurer.change-case
code --install-extension xyz.local-history
code --install-extension zengxingxin.sort-js-object-keys
```

</details>

## 3. Setting files:

- [⚙️ settings.json](/assets/settings.json)
- [⌨️ keybindings.json](/assets/keybindings.json)
