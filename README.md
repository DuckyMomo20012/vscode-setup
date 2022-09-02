# My VSCode setup

> NOTE: You can check [my keybinding settings](/assets/keybindings.json).

## 1. Recommend extension list:

- **TabOut** (albert.TabOut):
- **Auto Add Brackets in String Interpolation** (aliariff.auto-add-brackets):
- **statusbar-commands** (anweber.statusbar-commands):
- **Print It** (bmalehorn.print-it):
- **htmltagwrap** (bradgashler.htmltagwrap):
- **Bracket Select** (chunsen.bracket-select):
- **GitLens — Git supercharged** (eamodio.gitlens):
- **Prettier** (esbenp.prettier-vscode):
- **Auto Rename Tag** (formulahendry.auto-rename-tag):
- **Toggler** (hideoo.toggler):
- **Image preview** (kisstkondoros.vscode-gutter-preview):
- **dotENV** (mikestead.dotenv):
- **Rewrap** (stkb.rewrap):
- **Code Spell Checker** (streetsidesoftware.code-spell-checker):
- **Error Lens** (usernamehw.errorlens):
- **Highlight Matching Tag** (vincaslt.highlight-matching-tag):
- **TODO Highlight** (wayou.vscode-todo-highlight):
- **Sort JS object keys** (zengxingxin.sort-js-object-keys):
- **Bracketeer** (pustelto.bracketeer):
- **Color Highlight** (naumovs.color-highlight):

## 2. All extensions:

> You can use the command below to install all extensions 👇.

<details>
<summary>Extension list</summary>

```bash
code --install-extension albert.TabOut
code --install-extension aliariff.auto-add-brackets
code --install-extension amatiasq.sort-imports
code --install-extension anweber.statusbar-commands
code --install-extension bmalehorn.print-it
code --install-extension bradgashler.htmltagwrap
code --install-extension chunsen.bracket-select
code --install-extension dbaeumer.vscode-eslint
code --install-extension eamodio.gitlens
code --install-extension esbenp.prettier-vscode
code --install-extension formulahendry.auto-rename-tag
code --install-extension GitHub.copilot
code --install-extension kisstkondoros.vscode-gutter-preview
code --install-extension liviuschera.noctis
code --install-extension mikestead.dotenv
code --install-extension mongodb.mongodb-vscode
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-vscode-remote.remote-ssh
code --install-extension ms-vscode-remote.remote-ssh-edit
code --install-extension ms-vscode.cpptools
code --install-extension natqe.reload
code --install-extension naumovs.color-highlight
code --install-extension pflannery.vscode-versionlens
code --install-extension Prisma.prisma
code --install-extension pustelto.bracketeer
code --install-extension stkb.rewrap
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension usernamehw.errorlens
code --install-extension vincaslt.highlight-matching-tag
code --install-extension voorjaar.windicss-intellisense
code --install-extension vscode-icons-team.vscode-icons
code --install-extension WakaTime.vscode-wakatime
code --install-extension wayou.vscode-todo-highlight
code --install-extension zengxingxin.sort-js-object-keys
```

</details>

<details>
<summary>Command to get all extensions</summary>

Unix:

```bash
code --list-extensions | xargs -L 1 echo code --install-extension
```

Windows (PowerShell, e. g. using Visual Studio Code's integrated Terminal):

```powershell
code --list-extensions | % { "code --install-extension $_" }
```

</details>

## 3. Setting files:

- [⚙️ settings.json](/assets/settings.json)
- [⌨️ keybindings.json](/assets/keybindings.json)
