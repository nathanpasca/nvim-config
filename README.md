# Neovim Configuration

My personal Neovim configuration using LazyVim. This setup is optimized for JavaScript/TypeScript development with a focus on a minimal and efficient workflow.

## Features

- 🎨 Sonokai color scheme (Andromeda style) with transparent background
- 🌲 File explorer with NvimTree
- 🔍 Fuzzy finding with Telescope
- 📝 LSP support for:
  - TypeScript/JavaScript
  - CSS/Tailwind
  - Lua
- ⚡ Git integration with LazyGit
- 🧪 Testing support with Neotest
- 🔄 HTTP client with rest.nvim
- 🛠️ Database UI with vim-dadbod
- 💻 Code completion with nvim-cmp
- 🔧 Format and lint with prettier & eslint

## Prerequisites

- Neovim >= 0.9.0
- Git
- A [Nerd Font](https://www.nerdfonts.com/) (for icons)
- [ripgrep](https://github.com/BurntSushi/ripgrep) (for Telescope live grep)
- Node.js & npm (for LSP servers)
- make (for telescope-fzf-native)
- [lazygit](https://github.com/jesseduffield/lazygit) (for git integration)

## Installation

1. Backup your existing Neovim configuration if you have one:
```bash
# required
mv ~/.config/nvim ~/.config/nvim.bak
# optional but recommended
mv ~/.local/share/nvim ~/.local/share/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
mv ~/.cache/nvim ~/.cache/nvim.bak
```

2. Clone this repository:
```bash
git clone https://github.com/nathanpasca/nvim-config.git ~/.config/nvim
```

3. Start Neovim:
```bash
nvim
```

LazyVim will automatically install all plugins on the first start.

## Key Mappings

### General
- `<Space>` - Leader key
- `<Leader>w` - Save file
- `<Leader>q` - Quit
- `<Leader>Q` - Force quit

### File Navigation
- `;f` - Find files
- `;r` - Live grep
- `\\` - List buffers
- `;;` - Resume last telescope picker
- `sf` - File browser
- `<Leader>f` - NvimTree find file
- `<Leader>t` - NvimTree toggle

### Window Management
- `ss` - Split window horizontally
- `sv` - Split window vertically
- `sh`, `sj`, `sk`, `sl` - Navigate windows
- `<C-S-h>`, `<C-S-j>`, `<C-S-k>`, `<C-S-l>` - Resize windows

### Development
- `;c` - Open LazyGit
- `<Leader>d` - Toggle database UI
- `\r` - Run HTTP request under cursor
- `;tt` - Run test file
- `;tr` - Run nearest test
- `;ts` - Toggle test summary
- `<Leader>rn` - Rename symbol
- `<Leader>r` - Refactoring menu (in visual mode)

## Directory Structure
```
~/.config/nvim/
├── lua/
│   └── plugins/           # Plugin configurations
├── init.lua              # Main configuration file
└── lazy-lock.json       # Plugin version lock file
```

## Customization

You can modify any of the configuration files in the `lua/plugins/` directory to customize your setup. After making changes, restart Neovim and run `:Lazy sync` to ensure all plugins are up to date.

## Acknowledgments

This configuration is based on [LazyVim](https://github.com/LazyVim/LazyVim) and includes various plugins from the Neovim community.
