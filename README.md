<!-- <img width="100%" src="doc/preview.svg" /> -->

<div align="center">
  <h1 align="center">nvim-api.nvim<img width="32" src="https://neovim.io/logos/neovim-mark-flat.png" align="right" /></h1>
</div>

<!-- Use badges from https://shields.io/badges/ -->
[![PayPal](https://img.shields.io/badge/-PayPal-880088?style=flat-square&logo=pay&logoColor=white&label=DONATE)](https://www.paypal.me/biteofpie)
[![License](https://img.shields.io/badge/-007744?style=flat-square&label=LICENSE)](https://github.com/hinell/fossil-license)

> _Cross-runtime OOP based nvim API wrapper_

## ⚡FEATURES
- OOP helper wrapper for autocmds
- OOP helper wrapper for user comands

## 🔒REQUIREMENTS
- [Neovim 0.8.3+](https://github.com/neovim/neovim)

## 📦 INSTALL
Use your favorite plugin manager, and then call.

lazy.vim:
```lua
require("lazy").setup({
    {
        "hinell/nvim-api.nvim"
        dependencies={},
        config = function()
            require("nvim-api").setup()
        end
    }
})
```

> **WARNING**
> Packer.nvim is archived

packer.nvim:
```lua
-- /home/alex/.config/nvim/lua/user/init.lua
packer.setup(function(use)
    use ({
        "hinell/nvim-api.nvim"
        , config = function()
            require("nvim-api").setup()
        end
    })
end)
```

vim-plug:
``` vim
Plug "hinell/nvim-api.nvim"
```


## 🚀 USAGE

${USAGE}

## ⚙️ CONFIGURATION

* Default configuration can be found at [lua/nvim-api/config.lua](lua/nvim-api/config.lua)
* `require("nvim-api").setup({ })`
* [`:h nvim-api`](doc/nvim-api.txt)

----
<!-- ### THANKS -->
### [DOCUMENTATION]

Run `h nvim-api`

[DOCUMENTATION]: doc/index.md 'User documentation'

### [CONTRIBUTING]

[CONTRIBUTING]: CONTRIBUTING.md 'Devloper documentation (see also source code files)'

### [SUPPORT DISCLAIMER][SD]
[SD]: #production-status--support 'Production use disclaimer & support info'

_NO GUARANTEES UNTIL PAID. This project is supported and provided AS IS. See also [LICENSE]._

[LICENSE]: LICENSE

### SEE ALSO
* [@hinell/lsp-timeout.nvim](https://github.com/hinell/lsp-timeout.nvim) -  halt LSP servers when you leave nvim window
* [@hinell/duplicate.nvim](https://github.com/hinell/duplicate.nvim) - duplicate selection
* [@hinell/nvim-tree-git.nvim](https://github.com/hinell/nvim-tree-git.nvim) - GIT integration plugin for infamous file explorer

----
December 24, 2023<br/>
Copyright © 2023 - Alexander Davronov, et.al.<br/>
