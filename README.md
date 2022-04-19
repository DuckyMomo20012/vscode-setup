# My VSCode setup

> NOTE: You can check [my keybinding settings](/assets/keybindings.json).

## 1. Featured extension list:

### 📦 🤌 (Recommend) **TabOut** (albert.TabOut):

> 💅: This extension is very handy, you can use tab to get
> out bracket or quotes.

> 👎: Sometimes, it can conflict with intellisense.

**Keyboard shortcut:** <kbd>Tab</kbd>

---

### 📦 **Auto Add Brackets in String Interpolation** (aliariff.auto-add-brackets):

> 👎: Doesn't work with multiline template string.

---

### 📦 **statusbar-commands** (anweber.statusbar-commands):

> 💅: My favorite extension, I don't have to combine keybindings
> <kbd>Ctrl+Shift+P</kbd> to execute commands.

> 👎: Icon and text is not center aligned.

**Demo:**

![statusbar-command-demo](/assets/statusbar-command-demo.png)

**Settings:**

<details>
<summary>settings.json</summary>

```json
{
  "statusbar_command.commands": [
    {
      "alignment": "left",
      "color": "#EA6962",
      "command": "editor.action.fontZoomReset",
      "id": "reset-zoom",
      "name": "Reset Font Zoom",
      "priority": -1,
      "text": "$(refresh)",
      "tooltip": "Resest font zoom"
    },
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
    {
      "alignment": "left",
      "color": "#89B482",
      "command": "sortJsObjectKeys.sortJsObjectKeys",
      "id": "sort-object-keys",
      "name": "Sort JS object keys (Extension)",
      "priority": -5,
      "text": "$(arrow-down)$(json)",
      "tooltip": "Sort JS object keys (ascending)"
    },
    {
      "alignment": "left",
      "color": "#7DAEA3",
      "command": "editor.action.sortLinesAscending",
      "id": "sort-line-ascending",
      "name": "Sort Lines Ascending",
      "priority": -6,
      "text": "$(arrow-down)$(list-selection)",
      "tooltip": "Sort Lines Ascending"
    },
    {
      "alignment": "left",
      "color": "#EA6962",
      "command": "extension.changeCase.commands",
      "id": "change-case",
      "name": "Change Case (Extension)",
      "priority": -7,
      "text": "$(wand)$(text-size)",
      "tooltip": "Quickly change the case of the current selection or current word"
    },
    {
      "alignment": "left",
      "color": "#E78A4E",
      "command": "editor.emmet.action.removeTag",
      "filterLanguageId": "html|javascriptreact|markdown",
      "id": "remove-tag",
      "name": "Remove HTML Tag (Emmet)",
      "priority": -8,
      "text": "$(trash)$(code)",
      "tooltip": "Remove HTML tag"
    },
    {
      "alignment": "left",
      "color": "#D8A657",
      "command": "extension.htmlTagWrap",
      "filterLanguageId": "html|javascriptreact|markdown",
      "id": "htmlwrap",
      "name": "HTML Tag Wrap (Extension)",
      "priority": -9,
      "text": "$(add)$(code)",
      "tooltip": "Wraps selection in HTML tag"
    },
    {
      "alignment": "left",
      "color": "#A9B665",
      "command": "editor.emmet.action.splitJoinTag",
      "filterLanguageId": "html|javascriptreact|markdown",
      "id": "split-join-tag",
      "name": "Split/Join HTML Tag (Emmet)",
      "priority": -10,
      "text": "$(merge)$(code)",
      "tooltip": "Split/Join HTML tag"
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

**Keyboard shortcut:** <kbd>Alt+[</kbd>

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

**Keyboard shortcut:** <kbd>Alt+/</kbd>

---

### 📦 🤌 (Recommend) **Bracket Select** (chunsen.bracket-select):

> 💅: I use it frequently, very very handy extension.

> 👎: Undo select conflict with GeForce Experience 🤷‍♂️.

**Keyboard shortcut:**

- Select inside bracket: <kbd>Alt+A</kbd>.
- Undo select bracket: <kbd>Alt+Z</kbd>.
- Select include bracket: <kbd>Ctrl+Alt+A</kbd>.

---

### 📦 **GitLens — Git supercharged** (eamodio.gitlens):

---

### 📦 **HTML CSS Support** (ecmel.vscode-html-css):

---

### 📦 🤌 (Recommend) **Prettier** (esbenp.prettier-vscode):

**Keyboard shortcut:** <kbd>Shift+Alt+F</kbd>

---

### 📦 **Auto Rename Tag** (formulahendry.auto-rename-tag):

> 💅: VSCode built-in setting: "editor.linkedEditing" isn't good enough.

---

### 📦 ~~**Dummy Text Generator** (gurayyarar.dummytextgenerator)~~ VSCode has Emmet for this:

---

### 📦 **Toggler** (hideoo.toggler):

**Settings:**

<details>
<summary>settings.json</summary>

```json
{ "toggler.toggles": [["let", "const"]] }
```

</details>

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

**Keyboard shortcut:** <kbd>Alt+\ </kbd>

---

### 📦 **Center Editor Window** (kaiwood.center-editor-window):

<details>
<summary>Another way: keybindings.json</summary>

```json
[
  {
    "key": "alt+v",
    "command": "cursorMove",
    "args": {
      "to": "viewPortCenter"
    }
  }
]
```

</details>

**Keyboard shortcut:** <kbd>Ctrl+L</kbd>

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

### 📦 ~~🤌 (Recommend) **Vietnamese - Code Spell Checker** (streetsidesoftware.code-spell-checker-vietnamese)~~ Doesn't necessary:

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

- Indent one space: <kbd>Space</kbd>
- Reverse indent one space: <kbd>Shift+Space</kbd>

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

> 👎: Sometimes it doesn't work. (Update: You should select content including the
> bracket "{}")

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

- <kbd>Alt+'</kbd> : Swap quotes.
- <kbd>Alt+;</kbd> : Swap brackets.
- <kbd>Shift+Alt+'</kbd> : Remove quotes.
- <kbd>Shift+Alt+;</kbd> : Remove brackets.

---

### 📦 🤌 (Recommend) **Color Highlight** (naumovs.color-highlight):

**Demo:**

![color-highlight-demo](/assets/color-highlight-demo.png)

---

### 📦 🤌 (Super Recommend) **Gruvbox Material** (sainnhe.gruvbox-material):

---

### 📦 ~~**Incrementor** (nmsmith89.incrementor)~~ VSCode has built-in commands for this:

> 💅: Highly recommend.

> 👎: You have to select the whole number to increase.

**Settings:**

<details>
<summary>keybindings.json</summary>

```json
[
  {
    "key": "ctrl+;",
    "command": "editor.emmet.action.decrementNumberByOne",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+'",
    "command": "editor.emmet.action.incrementNumberByOne",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+alt+;",
    "command": "editor.emmet.action.decrementNumberByTen",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+alt+'",
    "command": "editor.emmet.action.incrementNumberByTen",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+shift+alt+;",
    "command": "editor.emmet.action.decrementNumberByOneTenth",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+shift+alt+'",
    "command": "editor.emmet.action.incrementNumberByOneTenth",
    "when": "editorTextFocus"
  }
]
```

</details>

**Keyboard shortcut:**

- <kbd>Ctrl+'</kbd> : Increase by 1.
- <kbd>Ctrl+;</kbd> : Decrease by 1.
- <kbd>Ctrl+Alt+'</kbd> : Increase by 10.
- <kbd>Ctrl+Alt+;</kbd> : Decrease by 10.
- <kbd>Ctrl+Shift+Alt+'</kbd> : Increase by 0.1.
- <kbd>Ctrl+Shift+Alt+;</kbd> : Decrease by 0.1.

---

### 📦 ~~🤌 (Recommend) **Subword Navigation** (ow.vscode-subword-navigation)~~ VSCode has built-in commands for this:

**Keyboard shortcut:**

- <kbd>Alt+➡️</kbd> : Cursor Subword Right
- <kbd>Shift+Alt+➡️</kbd> : Cursor Subword Right Select
- <kbd>Alt+⬅️</kbd> : Cursor Subword Left
- <kbd>Shift+Alt+⬅️</kbd> : Cursor Subword Left Select
- <kbd>Alt+Backspace</kbd> : Delete Subword Left
- <kbd>Alt+Delete</kbd> : Delete Subword Right

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
code --install-extension dbaeumer.vscode-eslint
code --install-extension Domi.dbux-code
code --install-extension eamodio.gitlens
code --install-extension esbenp.prettier-vscode
code --install-extension formulahendry.auto-rename-tag
code --install-extension hideoo.toggler
code --install-extension kaiwood.center-editor-window
code --install-extension kisstkondoros.vscode-gutter-preview
code --install-extension mikestead.dotenv
code --install-extension mongodb.mongodb-vscode
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-toolsai.jupyter
code --install-extension ms-toolsai.jupyter-keymap
code --install-extension ms-toolsai.jupyter-renderers
code --install-extension ms-vscode-remote.remote-ssh
code --install-extension ms-vscode-remote.remote-ssh-edit
code --install-extension ms-vscode.cpptools
code --install-extension ms-vsliveshare.vsliveshare
code --install-extension natqe.reload
code --install-extension naumovs.color-highlight
code --install-extension patbenatar.advanced-new-file
code --install-extension pflannery.vscode-versionlens
code --install-extension Prisma.prisma
code --install-extension pustelto.bracketeer
code --install-extension redhat.vscode-xml
code --install-extension sainnhe.gruvbox-material
code --install-extension stkb.rewrap
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension usernamehw.errorlens
code --install-extension usernamehw.indent-one-space
code --install-extension vincaslt.highlight-matching-tag
code --install-extension voorjaar.windicss-intellisense
code --install-extension vscode-icons-team.vscode-icons
code --install-extension WakaTime.vscode-wakatime
code --install-extension wayou.vscode-todo-highlight
code --install-extension wmaurer.change-case
code --install-extension xyz.local-history
code --install-extension zengxingxin.sort-js-object-keys
```

</details>

<details>
<summary>Command to get all extensions</summary>

```powershell
code --list-extensions | % { "code --install-extension $_" }
```

Ref: [link](https://stackoverflow.com/questions/35773299/how-can-you-export-the-visual-studio-code-extension-list)

</details>

## 3. Setting files:

- [⚙️ settings.json](/assets/settings.json)
- [⌨️ keybindings.json](/assets/keybindings.json)
