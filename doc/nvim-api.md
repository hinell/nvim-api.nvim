## OVERVIEW
Cross-runtime OOP based nvim API wrapper

REQUIREMENTS
- Neovim 0.8.3+: https://github.com/neovim/neovim

## INSTALL
Use your favorite package manager (Packer, Plug, Lazy.nvim etc.)
```
hinell/nvim-api
```

lazy.nvim:
```lua
require("lazy").setup({
    {
        "hinell/nvim-api",
        dependencies={},
        config = function()
            -- see setup() below
        end
    }
})
```

> **WARNING**
> Packer.nvim is archived

pckr.nvim:
packer.nvim:
```lua
    use({
        "hinell/nvim-api",
        requires={},
        config = function()
            -- see setup() below
        end
    })
```

## UPDATE
You may want to reinstall this plugin manually: because of specific dev-apprach,
the plugin repo may be force-rebased, rendering all previous commits obsolete.

## API

### CONFIGURATION

### EXAMPLES

### KEYMAP
NO keymap is setup by default.

```lua
vim.keymap.set({ "n" }, "<ABC>"   ,"<CMD>COMMAND<CR>")
```

<!-- #### LEGEND -->

-----
December 24, 2023<br/>
Copyright © 2023 - Alexander Davronov, et.al.<br/>
