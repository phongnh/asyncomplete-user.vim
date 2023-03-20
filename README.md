# asyncomplete-user.vim

A fork from [asyncomplete-omni.vim](https://github.com/yami-beta/asyncomplete-omni.vim) to support `completefunc` source for [asyncomplete.vim](https://github.com/prabirshrestha/asyncomplete.vim)

## Install

```vim
Plug 'prabirshrestha/asyncomplete.vim'
Plug 'phongnh/asyncomplete-user.vim'
```

## Register asyncomplete-user.vim

```vim
autocmd User asyncomplete_setup call asyncomplete#register_source(asyncomplete#sources#user#get_source_options({
\ 'name': 'user',
\ 'allowlist': ['*'],
\ 'blocklist': ['c', 'cpp', 'html'],
\ 'completor': function('asyncomplete#sources#user#completor'),
\ 'config': {
\   'show_source_kind': 1,
\ },
\ }))
```

### Config

#### `show_source_kind`

Add `o` kind label to `'menu'`
