+++
date = '2025-07-03T09:01:27+02:00'
draft = false
title = 'How to Add Ip to Linux Prompt'

tags = ["Linux"]
categories = ["IT"]
ShowToc = true

+++

Assumption
1. you are using oh-my-zsh
2. you are using ys as theme

# create a helper function

edit the ys theme file: `~/.oh-my-zsh/themes/ys.zsh-theme`

add the following function to the abovementioned file
```bash
function get_ip_address {
  # Get primary IPv4 address
  echo "$(ipconfig getifaddr en0 2>/dev/null || hostname -I | awk '{print $1}')"
}

```
# use the helper function 

use the function, `get_ip_address`, in the `PROMPT`

```bash
PROMPT="
%{$terminfo[bold]$fg[blue]%}#%{$reset_color%} \
%(#,%{$bg[yellow]%}%{$fg[black]%}%n%{$reset_color%},%{$fg[cyan]%}%n) \
%{$reset_color%}@ \
%{$fg[green]%}$(get_ip_address) \
%{$reset_color%}in \
%{$terminfo[bold]$fg[blue]%}%d%{$reset_color%}\
${hg_info}\
${git_info}\
${svn_info}\
${venv_info}\
 \
[%*] $exit_code
%{$terminfo[bold]$fg[red]%}$ %{$reset_color%}"
```