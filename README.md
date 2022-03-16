# Vim Guide

Welcome to my guide to [Vim](https://www.vim.org/)! All of the code in this repository, including these Markdown files, will be written with the [Vim extension for VS Code](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim).

## Getting started

To get started, install the extension. And...you're pretty much done! From here, you can figure out your own preferences, if you need to enable macros, etc. One modification that I strongly recommend is to enable "tab" functionality while in Vim's readonly mode. To do this, simply go to your `keybindings.json` file in VS Code. An easy way to get to this file is to **ONLY USE YOUR KEYBOARD**. This is a Vim guide after all, so you may as well get used to abandoning that mouse of yours, until it's time to play Valorant, of course. To open `keybindings.json`, I recommend doing the following:

- `CTRL + SHIFT + P`: this opens up the VS Code command palette
- Type in "open key": at this point, the `keybindings.json` file should pop up as one of the options
- Hit `ENTER` if the option to open `keybindings.json` is already selected
- Otherwise, use the down arrow key as many times as necessary to select it

Congratulations! You're on your way to becoming a true keyboard warrior. But not *that* type of keyboard warrior. I'd strongly advise against having virtual arguments with strangers on the internet over social media platforms. Trust me. Now that we've gotten to the `keybindings.json` file, let's enable "tab" functionality for readonly mode while in Vim. You've probably already noticed how your normal cursor in VS Code has disappared, only to be transformed into a blinking highlight, like those found in terminals. Since this is a guide to Vim, I'll be writing up documentation on what I believe to be the most important commands, but for now, here are a few basic ones to get you started (and actually be able to make some changes to `keybindings.json`).

- `i` : Enter insert mode on the left side of the readonly highlight
- `a` : Enter insert mode on the right side of the readonly highlight
- `CTRL + C` : Exit insert mode (the main command is `ESC`, but since we're programmers, hitting the "copy" macro is already hard-wired into our brains, so why not stick with that one?)
- `j` : Go down one line
- `k` : Go up one line
- `l` : Go right one character
- `h` : Go left one character

There are quite a few more basic commands, but this is a good starting point. Getting used to the directions associated with your home row keys and quickly toggling between readonly and insert mode should be your initial goal. Now let's insert some JSON data:

```
[
   {
       "key": "tab",
       "command": "tab",
       "when": "editorTextFocus && !editorTabMovesFocus"
   },
   {
        "key": "shift+tab",
        "command": "outdent",
        "when": "editorTextFocus && !editorTabMovesFocus"
   }
]
```

The brackets may already be in the file.

But that's pretty much it! At this point, experiment with Vim in VS Code as much as you want. You can do what I'm doing right now; writing some simple Markdown can get you familiarized with the basic commands. For the next step, we're going to learn more advanced Vim commands by doing them.

## Vim Tutor

Vim Tutor is just some simple text that is designed to teach its user about Vim commands. In fact, you can find the text at this [link](http://www2.geog.ucl.ac.uk/~plewis/teaching/unix/vimtutor). However, it's only useful if you actually use it *in* Vim, or in other words, follow the tutorial by actually using keyboard commands. Here's a quick rundown on how to install Vim for Vim Tutor:

1. Go to [Vim downloads](https://www.vim.org/download.php)
2. Download the appropriate installer for your OS
3. Run the downloaded installer as an administrator
4. During installation, make sure to check the box that creates `.bat` files
5. Once installation is complete, open a terminal and type this command: `vimtutor`

You should now be looking at Vim Tutor's text in gVim. The rest is self-explanatory. Follow the tutorial, and make sure you don't just read the content, actually *do* the content! Though I'd like to give a brief overview of the individual lessons in Vim Tutor, I think that it's best to let the material speak for itself. Make sure to do the parts of the tutorial that make you perform commands beyond the gVim client as well (saving files with Vim)! Besides, the fact that Vim Tutor includes countless emphases on learning by *doing* rather than memorization only affirms how important it is to work through the tutorial entirely.

## More Vim Commands

Now I know that you can find every single Vim command that exists just by doing a quick Google search, so I'm not going to be redundant here by listing all of those commands. Instead, I'm going to list some more commands that I've found to be very useful thus far. Extending beyond those initial commands listed earlier is important, although becoming a complete expert on absolutely everything that Vim can do is probably unnecessary. I would only pursue becoming a complete Vim expert out of passion, rather than out of a pursuit of efficacy.

- `$` : Jump to the end of the line
- `A` : Jump to the end of the line and enter insert mode on the right side of the readonly highlight
- `0` : Jump to the start of the line
- `I` : Jump to the start of the line and enter insert mode on the left side of the readonly highlight
- `gg` : Jump to the start of the file
- `G` : Jump to the end of the file
- `yy` : Copy the current line to Vim register
- `p` : Go down one line and paste from Vim register
- `P` : Paste on current line from Vim register
- `v` : Enter visual mode (select)
- `V` : Enter visual line mode (select entire lines at a time)
- `e` : Skip to the end of the next word
- `w` : Skip to the beginning of the next word
- `b` : Skip to the beginning of the previous word
- `{` : Go back one section (Vim finds blank lines)
- `}` : Go forward one section
- `x` : Delete current character
- `d` : Delete command, can be combined with numbers and motions (for example, `d2e` deletes the next two words), most commonly used after selecting a chunk of text, also saves to Vim register
- `dd` : Delete current line and save it to Vim register
- `o` : Add a line below the current line and go into insert mode
- `O` : Add a line above the current line and go into insert mode
- `gj` : Move down a line in multi-line text
- `gk` : Move up a line in multi-line text
- `%` : Toggle between brackets, parentheses, or curly braces when hovering over them
- `^` : Jump to the first non-blank character of the line
- `[number]gg` : Jump to line [number] in the file (using `G` after the number also works)
- `u` : Undo
- `CTRL + R` : Redo