# enjoy-life

> 💙 A tiny shell plugin that shows a random reason to enjoy life every time you open a new terminal.

Available for **Fish**, **Zsh**, **Bash** and **PowerShell**.

---

## Fish

### Install with Fisher

```fish
fisher install paulrobu/enjoy-life
```

### Uninstall

```fish
fisher remove paulrobu/enjoy-life
```

---

## Zsh

### Install with zinit

```zsh
zinit light paulrobu/enjoy-life
```

### Install with antidote

Add to your `.zsh_plugins.txt`:

```
paulrobu/enjoy-life
```

### Install with Oh My Zsh

```zsh
git clone https://github.com/paulrobu/enjoy-life \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/enjoy-life
```

Then add `enjoy-life` to the `plugins=(...)` list in your `~/.zshrc`.

### Uninstall

Remove the plugin from your plugin manager, or remove the `source` line from `~/.zshrc`.

---

## Bash

### Install

```bash
git clone https://github.com/paulrobu/enjoy-life ~/.enjoy-life
echo 'source ~/.enjoy-life/enjoy-life.bash' >> ~/.bashrc
source ~/.bashrc
```

### Install with bash-it

```bash
cp ~/.enjoy-life/enjoy-life.bash \
  ~/.bash_it/plugins/available/enjoy-life.plugin.bash
bash-it enable plugin enjoy-life
```

### Uninstall

Remove the `source` line from `~/.bashrc`, or disable via your plugin manager.

---

## PowerShell

Works on Windows, macOS, and Linux (PowerShell 5.1+).

### Install

```powershell
git clone https://github.com/paulrobu/enjoy-life "$HOME/.enjoy-life"
```

Then add this line to your PowerShell profile (`$PROFILE`):

```powershell
. "$HOME/.enjoy-life/enjoy-life.ps1"
```

To open your profile for editing:

```powershell
notepad $PROFILE        # Windows
code $PROFILE           # VS Code (any platform)
```

If your profile doesn't exist yet, create it first:

```powershell
New-Item -ItemType File -Path $PROFILE -Force
```

### Uninstall

Remove the `. "$HOME/.enjoy-life/enjoy-life.ps1"` line from your `$PROFILE`.

---

## Preview

```
💙 See a sunset that sets the sky on fire
💙 Looking back on this moment in 10 years and knowing you made it
```

---

## Contributing

### Adding or editing reasons

All reasons live in a single file: [`reasons.txt`](./reasons.txt) — one reason per line, blank lines and `#` comments are ignored.

After editing, regenerate all shell files by running:

```bash
./build.sh
```

This overwrites `conf.d/enjoy_life.fish`, `enjoy-life.plugin.zsh`, `enjoy-life.bash`, and `enjoy-life.ps1` from `reasons.txt`. Never edit those files directly — your changes will be lost on the next build.

PRs welcome — new reasons, new shells, bug fixes.

