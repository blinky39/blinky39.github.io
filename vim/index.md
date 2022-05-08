## vim stuff here

### setting

[using ultisnips in coc](https://github.com/neoclide/coc-snippets)

### short way: map your <tab> like this and run `:CocInstall coc-snippets`
''' vim
inoremap <silent><expr> <TAB>
      \ pumvisible() ? coc#_select_confirm() :
      \ coc#expandableOrJumpable() ? "\<C-r>=coc#rpc#request('doKeymap', ['snippets-expand-jump',''])\<CR>" :
      \ <SID>check_back_space() ? "\<TAB>" :
      \ coc#refresh()

function! s:check_back_space() abort
  let col = col('.') - 1
  return !col || getline('.')[col - 1]  =~# '\s'
endfunction

let g:coc_snippet_next = '<tab>'

'''
### add custom snippets: see coc-snippets README.md QA
