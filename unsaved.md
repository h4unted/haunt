[vimwiki](vimwiki)

:unsaved:

```lua

-- To stop unwanted saves in your ~/.config/nvim/init.lua file, type: 

vim.cmd([[
set noswapfile
augroup deleteprevbuffer
    autocmd!
    autocmd BufAdd *.md bp|bd!
augroup END
]])

-- And in your ~/.config/nvim/plugin/vimwiki.lua file, type:

vim.g.vimwiki_autowriteall = 0 

```



