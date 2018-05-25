# iTerm
- Tmux 100% the time
- Tab-switching goes to desktop occasionally

# Shell
- Move to ZSH
- Multiline history entries are only partially matched by C-r
- stty -icanon ixany
- Fix and split .dir_colors for direct-color and 16-color

# Git
- Mergetool
- `git add --patch .` should work to patch add unknown and known files
- Unable to clone work repos from work dir

# Tmux
- Prevent using alt screen
- Double click should highlight
- Window close should reattach to right-adjacent window
- %if FORMAT cannot access client or session information
- Normalize word seps in command- and copy-mode (include _ and -)
- Normalize word boundary stickiness when switching left/right
- Sync tmux <-> tmux/vim clipboards?

# Vim
- Word jumping broken in command-mode outside tmux
- Git line-level information (in the "gutter"?)
- Visual select not picking up last char
- Completion
- FZF
- Grepper
- Goto by FZF pathname search
- Goto by Grepper content search
- Goto by definition
- Run tests
- Handle upcase-word in all modes (Option-Up)
- Handle downcase-word in all modes (Option-Down)
- Handle twiddle-word in all modes instead? (Option-Up...Up...Up)
- Reverse history search in command mode
- Normalize word seps in command-mode (include _ and -)
- Sync vim <-> vim/tmux clipboards?
