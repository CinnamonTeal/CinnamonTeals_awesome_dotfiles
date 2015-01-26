README.md

USE .bash_profile NOT .bashrc!!

Load the shell dotfiles, and then some:
* ~/.path can be used to extend `$PATH`.
* ~/.extra can be used for other settings you don’t want to commit.
for file in ~/.{path,bash_prompt,exports,aliases,functions,extra}; do
	[ -r "$file" ] && source "$file"
done

The above function means that aliases, functions, and the prompt are defined in
eponymous dotfiles. This means if something breaks and you want to fix aliases,
for example, you have to edit the .aliases file. 

If you want to change the colors of your prompt, subl the .bash_prompt and look for
the PS1 settings at the bottom.

the dotfiles loaded by my .bash_profile are a frankenstein of variables copied 
from the .bash_profile gifted to me by the Flatiron school, the .bash_profile 
gifted to me by my friend Patrick, and some of my own modifications. 

Enjoy!