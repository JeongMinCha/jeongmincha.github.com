---
layout: post
title: My doftiles (vimrc, bash_profile)
---

### .vimrc
```
set nocp

" Indent setting
filetype plugin on
set tabstop=4
set shiftwidth=4
set expandtab

set nu
set ai                  " auto indenting
"set ci                  " c indenting
set history=100         " keep 100 lines of history
set ruler               " show the cursor position
syntax on               " syntax highlighting
set hlsearch            " highlight the last searched term
filetype plugin on      " use the file type plugins
highlight OverLength ctermbg=red ctermfg=white guibg=#592929
match OverLength /\%81v.\+/

" When editing a file, always jump to the last cursor position
autocmd BufReadPost *
\ if ! exists("g:leave_my_cursor_position_alone") |
\ if line("'\"") > 0 && line ("'\"") <= line("$") |
\ exe "normal g'\"" |
\ endif |
\ endif

```

### bash_profile
```
################ define colors #################
C_DEFAULT="\[\033[m\]"
C_WHITE="\[\033[1m\]"
C_BLACK="\[\033[30m\]"
C_RED="\[\033[31m\]"
C_GREEN="\[\033[32m\]"
C_YELLOW="\[\033[33m\]"
C_BLUE="\[\033[34m\]"
C_PURPLE="\[\033[35m\]"
C_CYAN="\[\033[36m\]"
C_LIGHTGRAY="\[\033[37m\]"
C_DARKGRAY="\[\033[1;30m\]"
C_LIGHTRED="\[\033[1;31m\]"
C_LIGHTGREEN="\[\033[1;32m\]"
C_LIGHTYELLOW="\[\033[1;33m\]"
C_LIGHTBLUE="\[\033[1;34m\]"
C_LIGHTPURPLE="\[\033[1;35m\]"
C_LIGHTCYAN="\[\033[1;36m\]"
C_BG_BLACK="\[\033[40m\]"
C_BG_RED="\[\033[41m\]"
C_BG_GREEN="\[\033[42m\]"
C_BG_YELLOW="\[\033[43m\]"
C_BG_BLUE="\[\033[44m\]"
C_BG_PURPLE="\[\033[45m\]"
C_BG_CYAN="\[\033[46m\]"
C_BG_LIGHTGRAY="\[\033[47m\]"

###############################################################################
#                                                                             #
#                             PATH setting                                    #
#                                                                             #
###############################################################################

###############################################################################
#                                                                             #
#                              PS1 setting                                    #
#                                                                             #
###############################################################################
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/\1/'
}
#export PS1="> $C_BLUE\h $C_RED[\t] $C_GREEN[\w] $C_DEFAULT"
export PS1="> $C_BLUE\u $C_RED[\t] $C_GREEN[\w] $C_DEFAULT"
export PS1=$PS1"$C_LIGHTYELLOW$(parse_git_branch) $C_DEFAULT\n\$ "
export CLICOLOR=1
export LSCOLORS=CxFxBxDxCxegedabagacad

###############################################################################
#                                                                             #
#                              aliases setting                                #
#                                                                             #
###############################################################################
# Git aliases
alias gst="git status"
alias glg="git log --oneline -10"
alias grf="git reflog -10"
alias gcm="git commit"
alias gdff="git diff"
alias gps="git push origin $(parse_git_branch)"
alias gpsf="git push -f origin $(parse_git_branch)"
alias gca="git commit --amend"
alias gchm="git checkout master"

# ls aliases
alias ls="ls -v"
alias ll="ls -lv"

# MacPorts Installer addition on 2014-10-24_at_23:03:15: adding an appropriate 
# PATH variable for use with MacPorts.
export PATH="/opt/local/bin:/opt/local/sbin:$PATH"
# Finished adapting your PATH environment variable for use with MacPorts.

```