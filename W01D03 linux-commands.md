# Linux commands


## What you’ll learn

By the end of this lesson, you will be familiar with the following:

- A little history of the command line.
- How to access the command line from your own computer.
- How to perform some basic file manipulation.
- A few other useful commands.
- How to chain commands together to make more powerful tools.
- The best way to use administrator powers.

## Linux commands 

The Linux command line is a text interface to your computer. Often referred to as the shell, terminal, console, prompt or various other names, it can give the appearance of being complex and confusing to use. Yet the ability to copy and paste commands from a website, combined with the power and flexibility the command line offers, means that using it may be essential when trying to follow instructions online, including many on this very website!

This lesson will teach you a little of the history of the command line, then walk you through some practical exercises to become familiar with a few basic commands and concepts. We’ll assume no prior knowledge, but by the end we hope you’ll feel a bit more comfortable the next time you’re faced with some instructions that begin “Open a terminal”.

## A brief history lesson

During the formative years of the computer industry, one of the early operating systems was called Unix. It was designed to run as a multi-user system on mainframe computers, with users connecting to it remotely via individual terminals. These terminals were pretty basic by modern standards: just a keyboard and screen, with no power to run programs locally. Instead they would just send keystrokes to the server and display any data they received on the screen. There was no mouse, no fancy graphics, not even any choice of colour. Everything was sent as text, and received as text. Obviously, therefore, any programs that ran on the mainframe had to produce text as an output and accept text as an input.

## Opean a terminal

you can find a launcher for the terminal by clicking on the Activities item at the top left of the screen, then typing the first few letters of “terminal”, “command”, “prompt” or “shell”. Yes, the developers have set up the launcher with all the most common synonyms, so you should have no problems finding it.

![terminal1](./img/terminal-1.png)

However you launch your terminal, you should end up with a rather dull looking window with an odd bit of text at the top, much like the image below. Depending on your Linux system the colours may not be the same, and the text will likely say something different, but the general layout of a window with a large (mostly empty) text area should be similar.

![terminal2](./img/terminal-2.png)

Let’s run our first command. Click the mouse into the window to make sure that’s where your keystrokes will go, then type the following command, all in lower case, before pressing the Enter or Return key to run it.

`   pwd   `

You should see a directory path printed out (probably something like `/home/YOUR_USERNAME` , then another copy of that odd bit of text.

![terminal3](./img/terminal-3.png)

From the root directory, the following command will move you into the “home” directory (which is an immediate subdirectory of `/`):

`   cd home  `,  `  pwd  `

To go up to the parent directory, in this case back to `/`, use the special syntax of two dots `..` when changing directory (note the space between `cd` and `..`, unlike in DOS you can’t just type `cd..` as one command):

`cd ..`, `pwd`

### Creating folders and files

In this section we’re going to create some real files to work with. To avoid accidentally trampling over any of your real files, we’re going to start by creating a new directory, well away from your home folder, which will serve as a safer environment in which to experiment:

`mkdir /tmp/testing`

`cd /tmp/testing`

* Notice the use of an absolute path, to make sure that we create the testing directory inside `/tmp`. Without the forward slash at the start the `mkdir` command would try to find a `tmp` directory inside the current working directory, then try to create a testing directory inside that. If it couldn’t find a `tmp` directory the command would fail.

In case you hadn’t guessed, `mkdir` is short for ‘make directory’. Now that we’re safely inside our test area (double check with `pwd` if you’re not certain), let’s create a few subdirectories:

`mkdir dir1 dir2 dir3`

There’s something a little different about that command. So far we’ve only seen commands that work on their own `cd, pwd` or that have a single item afterwards `cd /, cd ~/Desktop`. But this time we’ve added three things after the `mkdir` command. Those things are referred to as parameters or arguments, and different commands can accept different numbers of arguments. The `mkdir` command expects at least one argument, whereas the `cd` command can work with zero or one, but no more. See what happens when you try to pass the wrong number of parameters to a command:\

`mkdir`

`cd /etc ~/Desktop`

### Creating files using redirection

Our demonstration folder is starting to look rather full of directories, but is somewhat lacking in files. Let’s remedy that by redirecting the output from a command so that, instead of being printed to the screen, it ends up in a new file. First, remind yourself what the `ls` command is currently showing:

`ls`

Suppose we wanted to capture the output of that command as a text file that we can look at or manipulate further. All we need to do is to add the greater-than character `>` to the end of our command line, followed by the name of the file to write to:

`ls > output.txt`

This time there’s nothing printed to the screen, because the output is being redirected to our file instead. If you just run `ls` on its own you should see that the `output.txt` file has been created. We can use the `cat` command to look at its content:

`cat output.txt`

Okay, so it’s not exactly what was displayed on the screen previously, but it contains all the same data, and it’s in a more useful format for further processing. Let’s look at another command, `echo`:

`echo "This is a test"`

Yes, `echo` just prints its arguments back out again (hence the name). But combine it with a redirect, and you’ve got a way to easily create small test files:

`echo "This is a test" > test_1.txt`

`echo "This is a second test" > test_2.txt`

`echo "This is a third test" > test_3.txt`

`ls`

You should `cat` each of these files to check their contents. But `cat` is more than just a file viewer - its name comes from ‘concatenate’, meaning “to link together”. If you pass more than one filename to `cat` it will output each of them, one after the other, as a single block of text:

`cat test_1.txt test_2.txt test_3.txt`

