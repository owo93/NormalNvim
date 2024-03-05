<div align="center">
  <img src="https://github.com/NormalNvim/NormalNvim/assets/3357792/76197752-0947-4392-a6bd-a59d64319028"></img>
  <h1><a href="https://github.com/NormalNvim/NormalNvim">NormalNvim (fork)</a></h1>
  <h3>*✨ ~ ⭐ - A normal Neovim distro - ⭐ ~ ✨*</h3>
</div>

---

The space key shows [all you can do](https://github.com/NormalNvim/NormalNvim/wiki/basic-mappings)
![screenshot_2023-06-14_11-41-03_398515538](https://github.com/NormalNvim/NormalNvim/assets/3357792/af73f0b2-b56e-47d8-9bb8-f68b76e4b577)

## Install (Linux/MacOS)

```sh
# Strongly recommended: Fork the repo and clone YOUR fork.
git clone https://github.com/owo93/NormalNvim.git ~/.config/nvim
```

## Install (Windows PowerShell)

```sh
# Strongly recommended: Fork the repo and clone YOUR fork.
git clone https://github.com/owo93/NormalNvim.git $env:UserProfile\AppData\Local\nvim && nvim
```

## Distro features

- ⚡ **Lazy:** Plugins are loaded lazily, providing super fast performance.
- 😎 **Plugins are self-contained:** Allowing you to easily delete what you don't want.
- 🔋 **Batteries included:** Most [plugins](https://github.com/NormalNvim/NormalNvim/wiki/plugins) you will ever need are included and debugged by default. Get the best user experience out of the box and forget about nasty bugs in your Neovim config.
- 🤖 **IDE tools:** We ship [Compiler.nvim](https://github.com/Zeioth/compiler.nvim) (compiler), [DAP](https://github.com/mfussenegger/nvim-dap) (debugger), [Neotest](https://github.com/nvim-neotest/neotest) (test runner), and [Dooku.nvim](https://github.com/Zeioth/dooku.nvim) (docs generator)
- 🐞 **IDE parsers:** Linters, Formatters, LSP, Treesitter... preinstalled, preconfigured and ready to code for the top 12 most popular programming languages.
- 🔒 **Plugin version lock:** You can choose "stable" or "nightly" update channels. Or if you prefer, use :NvimFreezePluginVersions to create your own stable versions!
- 🔙 **Rollbacks:** You can easily recover from a nvim distro update using :NvimRollbackRestore
- 🔥 **Hot reload:** Every time you change something in your config, the changes are reflected on nvim on real time without need to restart.
- 📱 **Phone friendly:** You can also install it on Android Termux. Did you ever have a compiler in your pocket? 😉
- ⌨️ **Alternative mappings:** By default the distro uses qwerty, but colemak-dh can be found [here](https://github.com/NormalNvim/NormalNvim/wiki).
- ❤️ **We don't treat you like you are stupid:** Code comments guide you to easily customize everything. We will never [hide or abstract](https://i.imgur.com/FCiZvp2.png) stuff from you.

## Commands

| Command                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **:checkhealth base**         | Check the system dependencies you are missing.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **:NvimUpdateConfig**         | Pulls the latest changes from the current git repository of your nvim config. Useful to keep your config updated when you use it in more than one machine. If the updates channel is `stable` this command will pull from the latest available tag release in your github repository. Only tag releases starting by 'v', such as v1.0.0 are recognized. It is also possible to define a specific stable version in `2-lazy.lua` by setting the option `stable_version_release`. If the channel is `nightly` it will pull from the nightly branch. Note that uncommitted local changes in your config will be lost after an update, so it's important you commit before updating your distro config.  |
| **:NvimRollbackCreate**       | Creates a recovery point. It is triggered automatically when running `:NvimUpdateConfig`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **:NvimRollbackRestore**      | Uses git to bring your config to the state it had when `:NvimRollbackCreate` was called.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **:NvimReload**               | Hot reloads the config without leaving nvim. It can cause unexpected issues sometimes. It is automatically triggered when writing the files `1-options.lua` and `4-mappings`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **:NvimUpdatePlugins**        | Uses lazy to update the plugins.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **:NvimFreezePluginVersions** | Saves your current plugin versions into `lazy_versions.lua` in your config directory. If you are using the `stable` updates channel, this file will be used to decide what plugin versions will be installed, and even if you manually try to update your plugins using lazy package manager, the versions file will be respected. If you are using the `nightly` channel, the first time you open nvim, the versions from `lazy_versions.lua` will be installed, but it will be possible to download the last versions by manually updating your plugins with lazy. Note that after running this command, you can manually modify `lazy_versions.lua` in case you only want to freeze some plugins. |
| **:CloseNotifications**       | Close all notifications. This is automatically triggered by default when writing a buffer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **:NvimVersion**              | Prints the commit number of the current NormalNvim version.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

For more info, [read the wiki](https://github.com/NormalNvim/NormalNvim/wiki).
