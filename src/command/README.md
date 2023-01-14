# Command

- [`general command`](#general-command)
- [`mac os`](#mac-os)
- [`networking`](#networking)

[↑ top](#command)
<br><br><br><br><hr>

### `general command`

### eval command

<br>

This is equivalent to running the command ls -l directly on the command line.

```bash
x="ls -l"
eval $x
```

### source command

<br>

source command is used to execute commands from a script file in the current shell environment, rather than starting a
new shell, so any changes made to the environment will persist after the script is finished running.

```bash
source myscript.sh
```

<br>

**similar ways to execute shell script file:**

- `sh scriptname.sh` : This method will run the script regardless of the user's default shell
- `bash scriptname.sh` : This command runs the script using the bash shell
- `./scriptname.sh` : need to provide executed permission for the script (`chmod +x scriptname.sh`)
- `./scriptname` : if the script has execute permission and it has the appropriate shebang line, you can run it just by typing its name

[↑ top](#command)
<br><br><br><br><hr>

### `mac os`

<br>

> - open -a application: open app on mac by terminal
> - lauchctl [stop|list]: stop or list out all running services


[↑ top](#command)
<br><br><br><br><hr>

### `networking`

<br>

> - netstat -a: list down all listening port
> - telnet [ip:port]: ping ip with specified port


[↑ top](#command)
<br><br><br><br><hr>
