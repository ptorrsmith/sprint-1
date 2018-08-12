nano - file editor

nano file.txt creates and opens file.txt in nano editor

ctrl + o - saves file

ctrl + x - exit nano editor

nano ~/.bash_profile - for profile settings. e.g. echo "Hi Peter" for greeting

~ = users home directory
. means it's a hidden file

source ~/.bash_profile  - activates the changes in ~/.bash_profile (saves having to close and reopen terminal)

~/.bash_profile example lines

echo "hello Peter Torr"
alias pd "pwd"
alias ll="ls -la"
alias hy="history"

export USER="Jane Doe" - sets global environment variable $USER - available to all child sessions of this session. 

Note: $ENVIRONMENT_VARIABLE is always preceeded with $ to return the value of ENVIRONMENT_VARIABLE

export PS1=">> " - sets command prompt to ">> "

env - returns all environment variables
env | grep PATH - returns lines with the text PATH

