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

