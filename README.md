# hyph-vim
it comes from k-vim(https://github.com/wklken/k-vim)

if using colorscheme=solarized, you can set Terminal "Edit->Profiles:Background color='#00002B2B3636'
if using new vim-plugin, you can run as ":BundleInstall" after adding Bundle 'xxx/xxx' in vimrc.bundles. 

modify vim-ctrlspace/plugin/ctrlspace.vim: 
    function! <SID>ctrlspace_toggle(internal)
      " add by hyph
      let s:hyph_currentbuf = bufname("%")
      if s:hyph_currentbuf ==# "__Tagbar__" || s:hyph_currentbuf ==# "NERD_tree_1" 
        silent! exe "wincmd p"
      endif
