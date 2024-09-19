# List of dig related alias

Add the following alias to your shell .profile, .zshrc, or .bashrc etc

```shell

# Dig shortcuts
alias diga="dig a +short"
alias digc="dig cname +short"
alias digr="dig -x"
alias digm="dig mx +short"
alias digt="dig txt +short"
alias dign="dig ns +short"
# Print your WAN IP address
alias mw='dig +short myip.opendns.com @resolver1.opendns.com'

```
