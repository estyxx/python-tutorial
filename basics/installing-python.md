# Installing Python

It doesn't matter which operating system you use because Python runs
great on Windows, Mac OSX, Linux and many other operating systems.
However, installing and launching Python are done differently on
different operating systems, so just follow your operating system's
instructions.

Let's get started!

## Downloading and installing Python

### Windows

Installing Python on Windows is a lot like installing any other program.

1. Go to [the official Python website](https://www.python.org/).
2. Move your mouse over the blue Downloads button, but don't click it.
   Then click the button that downloads the latest version of Python.
3. Run the installer.
4. Make sure that the launcher gets installed and click Install Now.

    ![The py.exe launcher.](../images/py-exe.png)

### Mac OSX

At the time of writing this, Macs don't come with a Python 3 and you
need to install it yourself. To install python on your Mac please follow the instruction
[here](https://docs.python-guide.org/starting/install3/osx/).

### Linux

If you have a recent Linux distribution you already have Python 3, 
**there's no need to install anything**. To check if Python 3 is already on your operating 
system run: `python --version`.

If you need to install python 3 please follow the istructions behind:

#### Ubuntu/Debian

```
sudo apt-get update
sudo apt-get install python3.7
```

If you’re using another version of Ubuntu (e.g. the latest LTS release), we recommend using the deadsnakes PPA to install Python 3.7:
```
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt-get update
$ sudo apt-get install python3.7
```


#### Fedora/CentOS
```
sudo dnf install python3
```

## Running Python

Next we'll learn to run Python on a PowerShell or terminal. There are
several other ways to run Python, but if you learn this way now it's
going to make things easier later.

### Windows

1. Open a PowerShell from your start menu or start screen.
2. Type `py` and press Enter. You should see something like this:

    ![Python running in a PowerShell window.](../images/powershell.png)

### Other operating systems

1. Open a terminal. How exactly this is done depends on your operating
    system, but most operating systems have some way to search for
    programs. Search for a program called terminal and launch it.
2. Type `python3` and press Enter. You should see something like this:

    ![Running Python on my terminal.](../images/terminal.png)

    Your terminal probably looks different than mine, it's OK.

Now you can type `exit()` and press Enter to get out of Python. Or you
can just close the PowerShell or Terminal window.

## Summary

Now you should have Python installed, and you should be able run it.

***


[Previous](what-is-programming.md) | [Next](getting-started.md) |
[List of contents](../README.md#basics)
