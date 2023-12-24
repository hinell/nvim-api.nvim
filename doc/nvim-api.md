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

* `M.autocmds:enable({ "AutoCmdName" })`  
`M.autocmds:disable({ "AutoCmdName" })`  
`M.autocmds:toggle({ "AutoCmdName" })`  
This set of commands can be used to enable/disable user autocommands at runtime.
It takes two tables used by `nvim_create_autocmd`.

```lua
local napi = require("nvim-api")
local autocmds = {
	{
		"BufNew"
	},{
		pattern  = "*",
		once     = true,
		group    = "MyAuGroup",
		callback = function(auEvent)
			print("triggered when buffer is created")
		end
	}
}

-- Enable entire table of autocmds dynamically
napi.autocmds:enable(autocmds)
-- Toggle entire table of autocmds dynamically
napi.autocmds:toggle(autocmds)
```

* `M.commands:enable({ name = ..., })`  
`M.commands:disable({ name = ..., })`  
`M.commands:toggle({ name = ..., })`  
This set of commands can be used to enable/disable user commands at runtime.  
It takes the same user command spec table used by `nvim_create_user_command`

```lua
local napi = require("nvim-api")
 
local cmds = {
    {
        name   = "UserCommandX",
        action = function(args) print("test") end,
        opts = {
            desc  = "Example of user command",
            force = true,
            bar   = true,
            nargs = "?"
                -- complete = function() end
                -- preview = function() end
        }
    }
}
 
napi.commands:toggle(cmds) 
```

### CONFIGURATION

<!-- ### EXAMPLES -->

<!-- ### KEYMAP -->
<!-- NO keymap is setup by default. -->
<!---->
<!-- ```lua -->
<!-- vim.keymap.set({ "n" }, "<ABC>"   ,"<CMD>COMMAND<CR>") -->
<!-- ``` -->

<!-- #### LEGEND -->

-----
Copyright © 2023 - Alexander Davronov, et.al.<br/>
December 24, 2023<br/>
February 16, 2024<br/>
