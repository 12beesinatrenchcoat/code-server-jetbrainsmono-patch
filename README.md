# Code Server Font Patch

This fork ([original here!](https://github.com/tuanpham-dev/code-server-font-patch)) patches [code-server](https://github.com/cdr/code-server) to enable the loading of [JetBrains Mono](https://www.jetbrains.com/lp/mono/) in code-server.

## Installation

- Clone this repository.

```bash
git clone https://github.com/12beesinatrenchcoat/code-server-jetbrainsmono-patch.git
cd code-server-jetbrainsmono-patch
```

- Run this command (change `path-to-code-server` to your code-server path, leave it empty if you install code-server from installer or code-server is in `/usr/lib/code-server`):

```bash
sudo ./patch.sh [path-to-code-server]
```

Restart code-server, maybe do a hard reload (`Ctrl` + `F5`) or something. It should work!

### Settings

You may need to set font family in code-server settings:

```json
"editor.fontFamily": "'JetBrains Mono', 'Comic Sans MS', Consolas, 'Courier New', monospace",
"terminal.integrated.fontFamily": "'JetBrains Mono', 'Comic Sans MS', Consolas, 'Courier New', monospace",
```

~~Okay, well, maybe not that second one.~~

JetBrains Mono also has ligatures! Turn those on if you like them (or off if you don't).

```jsonc
"editor.fontLigatures": true, // or false!
```
