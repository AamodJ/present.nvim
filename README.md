# `present.nvim`

This plugin is for presenting markdown files

# Features: Neovim Lua Code Execution

Can execute lua codeblocks in the current slide

```lua
print('Hello World', 37)
```

# Features: Execute other Langs

Can execute code from any Language block
You will have to provide the executor in `opts.executors.<language>`
By default, only supports lua and python

```python
print('Hello World')
```
# Usage

```lua
require('present').start_presentation {}
```

Use `n` and `p` to navigate markdown slides
