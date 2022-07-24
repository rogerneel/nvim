# Nvim Config

Pure lua nvim config. Probably requires nvim 0.7+


## Installation

### nvim
Install nvim with brew on MacOS or otherwise.

`brew install nvim`

You're also going to need a nerd-font to support extended characters:
`brew tap homebrew/cask-fonts`
`brew install --cask font-hack-nerd-font`

Ensure `Hack Nerd Font Mono` is used in your terminal of choice. 
(e.g. iTerm2: Preferences->Profiles->Text->Font)

### Clone Repo
Git clone this repo into `~/.config` and make sure the directory name is `nvim` within that dir.

### Plugins
The first time you run `nvim`, you will see all the plugins install and an unreadable purple dialog box fire.

Once it's complete, press `q` and then exit nvim with a `:q`. Restart nvim.

Once you restart `nvim` in any file, you should see a fully themed editor.

For future editing and installing plugins:
```bash
  cd ~/.config/nvim/lua/user/
  nvim plugins.lua
  (optionally add more plugins)
  :w (save plugins.lua within nvim)
```
the plugins will auto-install upon file save, then `:q` in `nvim`.

### LSP
Open any file in `nvim` and run `:LspInstallInfo`

You should see a popup with an __Available Servers__ menu.

Scroll down to any package and hit `i` to install.

At a minimum, install:
```
jsonls          -- for JSON file editing
sumneko_lua     -- for editing these lua config files
```

Browse the packages for what you need, but I use:
```
cssls           -- for CSS
html            -- for markup
pyright         -- for Python development
tailwindcss     -- for Tailwind projects
tsserver        -- for JS and TS projects
```

Restart nvim and you should see the LSP engine running / autocompleting.

### Telescope
For full Telescope plugin capabilities, also need to install `ripgrep` and `fd`

`brew install ripgrep`
`brew install fd`

Within NeoVim, run `:checkhealth telescope` to make sure everything is in place.

## Acknowledgements

I learned a ton and used a lot from chris@machine's amazing YouTube instruction series:

 - [Neovim from Scratch](https://www.youtube.com/playlist?list=PLhoH5vyxr6Qq41NFL4GvhFp-WLd5xzIzZ)
 - [Associated Repo](https://github.com/LunarVim/Neovim-from-scratch)

