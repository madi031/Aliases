parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

killp(){
        port=$(lsof -i :"$1" -t)
        kill -9 $port
}

function title {
    echo -ne "\033]0;"$*"\007"
}

export JUNIT_HOME="$HOME/java"
export PATH="$PATH:$JUNIT_HOME"
export CLASSPATH="$CLASSPATH:$JUNIT_HOME/junit-4.12.jar:$JUNIT_HOME/hamcrest-core-1.3.jar"
export EDITOR=vi
export PS1='\u$(parse_git_branch)$ '

alias ote='cd Documents/ubuntu-sf/RAD_Shared/OTEapp/'

alias spof='vi ~/.bash_profile'
alias uspof='source ~/.bash_profile'
alias clr='clear'

alias rn='react-native'
alias rninit='react-native init'
alias rnios='react-native run-ios'
alias rnfbsdk='react-native install react-native-fbsdk && react-native link react-native-fbsdk'
alias rnredux='npm install --save react-redux redux'

alias sl='open -a "sublime text"'
alias coffee='open -a caffeine'

alias ginit='git init'
alias gland='git push -u origin'
alias gadd='git add'
alias gcmt='git commit'
alias gcln='git clone'
alias grm='git remote add'
alias grmc='git rm --cached -r'
alias grmr='git remote remove'
alias gst='git status'
alias gbc='git checkout -b'
alias branch='git checkout'
alias grsi='git add -u && git reset -- .gitignore'

alias y='yarn'
alias ya='yarn add'
alias ni='npm install'
alias ns='npm start'
alias ngn='ng new'
alias ngs='ng serve'
alias nggc='ng generate component'
alias nggd='ng generate directive'

alias crp='create-react-app'
