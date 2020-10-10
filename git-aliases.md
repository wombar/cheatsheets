# Git Aliases

Simple set of aliases to help make git life easiuer

#### List a (nicely formatted) history

`lg = log --graph --pretty=format:'%C(red)%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue) - %an%Creset' --abbrev-commit`
	
#### Remove a particular user from the history (i.e. CI Build User)

`lg2 = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue) - %an%Creset' --abbrev-commit --grep=\\[BUILD_ROBOT\\] --invert-grep`

#### ZSH Theme

`ZSH_THEME="af-magic"`
