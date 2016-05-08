Powerline style prompt for Zsh :: Customize & Fix
===============================
This is fork from https://github.com/carlcarl/powerline-zsh

Custom&fix by saika
fix charset of status bar

![Powerline-Zsh Screenshot](http://i.imgur.com/QfDe3yP.png)
![Powerline-Zsh Screenshot2](http://i.imgur.com/f1kQcLv.png)


Setup
===============================
	
    * Clone this repository somewhere
    ```shell
    git clone https://github.com/0xsaika/powerline-zsh
    ```	

	* Create a symlink to the python script in your home:
   
    ```shell
    ln -s <path/to/powerline-zsh.py> ~/powerline-zsh.py
    ```


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

Usage
===============================
	* powerline-zsh.py usage:

	```shell
	-h, --help  show this help message and exit
	--cwd-only  Hide parent directory
	--hostname  Show hostname at the begin
	-m <mode>   Choose icon font: default, compatible, patched or konsole.
	            Default is "default"
	```

Tips
===============================

	 * If you want change root indicator chk line 287

	'''python
	powerline.append(Segment(powerline, ' $', fg, bg))
	'''