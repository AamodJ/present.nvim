# `present.nvim`

This plugin is for presenting markdown files

# Features: Neovim Lua Code Execution

Can execute lua codeblocks in the current slide with `X`

```lua
print('Hello World', 37)
```

# Features: Execute other Langs

Can execute code from any Language block with `X`
You will have to provide the executor in `opts.executors.<language>`
By default, only supports lua and python

```python
print('Hello World')
```

# Installation

Install with your favourite package manager such as [folke/lazy.nvim](https://github.com/folke/lazy.nvim): 
```lua
{
    "AamodJ/present.nvim",
}
```
# Usage

```lua
require('present').start_presentation {}
```

Use `n` and `p` to navigate markdown slides, `q` to quit presenting

# Customization

Example setup

```lua
require("present").setup({
    -- List of executors go here
    -- language = binary
    -- binary can be <path_to_binary> or <name_of_binary> if the binary is in your runtimepath
    executors = {
        python = "python"
    }
})
vim.keymap.set("n", "<leader>pp", "<cmd>PresentStart<CR>", {
    -- If you have which-key installed
    -- desc = "Start [P]resentation" 
})
```

# Credits 

This project is inspired from TJ's advent of neovim youtube playlist: [Advent of Neovim - TJ DeVries](https://youtube.com/playlist?list=PLep05UYkc6wTyBe7kPjQFWVXTlhKeQejM&si=hdGGi1kMSkn9LKAG):

Github repo: [tjdevries/present.nvim](https://github.com/tjdevries/present.nvim):
