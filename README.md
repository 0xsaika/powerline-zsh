Powerline style prompt for Zsh
===============================

*Edit by saika

![Powerline-Zsh Screenshot](http://i.imgur.com/QfDe3yP.png)
![Powerline-Zsh Screenshot2](http://i.imgur.com/f1kQcLv.png)

*Setup
* Now add the following to your `.zshrc`:

    ```shell
    export TERM='xterm-256color'
    ```

	```shell
	function _update_ps1()
	{
	    export PROMPT="$(~/powerline-zsh.py $?)"
	}
	precmd()
	{
	    _update_ps1
	}
	```