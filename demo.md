# Laith's Essential Vim Motions Cheat Sheet!

# Primitives

## Modes

- Normal
- Insert
- Visual
- Command

# Normal Mode

## hjkl

[ ]        
        [ ] (below you'll see some different behavior when there are no spaces on a line)

    [ ]

## Vertical Movement

### Line Numbers + j/k

I recommend turning on relative line numbers! (Cmd + , -> Search Line Number -> Change from "on" to "relative")

Start here!




Jump here!

### { and } - paragraph jumps

Start here!
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc tempus nibh dapibus dolor faucibus rutrum. Cras lobortis elementum ultrices. Sed ac odio malesuada, congue leo ac, scelerisque ipsum. Praesent nec turpis at mauris malesuada rutrum non id nunc. Phasellus porttitor consectetur fermentum. Praesent aliquam sit amet lacus a dapibus. Donec rhoncus tincidunt dui et accumsan. Curabitur id pulvinar dui.

Mauris sit amet ante id ligula commodo facilisis. Praesent condimentum commodo elit, non congue odio facilisis sed. Donec gravida tincidunt bibendum. Donec varius turpis id libero egestas tristique a eu urna. Aliquam ultrices, nisl id suscipit sodales, ex nunc commodo sapien, vel tempus lectus velit id nulla. Quisque ligula neque, maximus quis enim sed, tempor dapibus risus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nunc id ipsum et nisl auctor blandit.

End here!

### CTRL-d CTRL-u - half page jumps

Start here!















Should be around here lol. Go back up!

### G and gg - full page jumps

Press capital G to jump to the bottom of the file

### Ctrl + o and Ctrl + i - go back to previous cursor position after action, go back to most recent position after action

Type G and then Ctrl - O

## Horizontal Movement

### $ and 0 - end of line, beginning of line

abcdefghijklmnopqrstuvwxyz

### f and F + ; and , - go to next character, jump to each

abcABCabcABCxyzXYZ          abc ABC xxYYZZ  more text here          more text all the way here 

### w, e, b, t (character) - word, end, back, till (character)

Sandbox is Northeastern's student-led software consultancy building software for researchers, professors, and the student community. We've helped academic researchers looking to collect experimental data, deans looking to analyze student data, and students looking to find the right classes. We work closely with clients to help them best leverage computation.

# Editing in Normal Mode

## x - delete character

delete the Capital letter

## r + character - replace character

replace the Capital letter with a lowercase

## d (motion) - delete 

DeleteWord  DeleteTillI 

You can also use d + line jumps (try d10j - "delete 10 down")

[ ] Cursor here
Delete
Delete
Delete
Delete
Delete
Delete
Delete
Delete
Delete
Delete

## dd - delete line

DeleteLine
DeleteLine
DeleteLine
DeleteLine

## y (action) - yank

yword

Same behavior as delete! yy yanks line, y10l yanks 10 characters to the right, etc.

## p - paste

Paste below! 

Note: Everything you DELETE in Vim, goes to your yank clipboard by default. You can change this to be your system clipboard instead

## u - undo

Delete me then undo

## Ctrl + r - redo

Delete me then undo then redo

# Insert Mode

Okay now it's time to type!

How do I get out of the fat cursor?

First, to ALWAYS go back to normal mode, press ESC

## i and a - insert mode to the left and right of cursor

Stay in visual mode! Navigate to the `console.log(` line. Jump to the `(` Press 'a', finish the line and then go back to normal mode

```js
console.log("hello world")
```

This time, navigate to the `)`, press 'i' and close the quote, then go back to normal mode

```js
console.log("hello world")
```

## I and A - insert mode to the beginning and end of the line

Navigate anywhere on the paragraph below, and add "sand " to the beginning and add " box" to the end. Remember, you need to go back to normal mode to do the 'A' motion

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc tempus nibh dapibus dolor faucibus rutrum. Cras lobortis elementum ultrices. Sed ac odio malesuada, congue leo ac, scelerisque ipsum. Praesent nec turpis at mauris malesuada rutrum non id nunc. Phasellus porttitor consectetur fermentum. Praesent aliquam sit amet lacus a dapibus. Donec rhoncus tincidunt dui et accumsan. Curabitur id pulvinar dui.

## o and O - insert mode below and above current line


Move cursor to me, add a word below this line by pressing 'o'


Move cursor to me, add a word above me by pressing 'O'


## c - cut

Cut shares the same behavior as YANK and DELETE, but it auto puts you in insert mode after

cword

c10j
CUT
CUT
CUT
CUT
CUT
CUT
CUT
CUT
CUT
CUT

cc and delete this entire line wow

To note: this also adds the content to your yank clipboard

## Bonus action that I didn't share! [d/y/c] [i/a] ["/'/(/{/a]

Like I have been saying, you can essentially speak english and understand these actions.

Let's [d]elete [i]nside the quotes["]. Move to the beginning of the line and try

```js
console.log("hello, world")
```

Let's [c]ut [a]round the paranthesis[)]. Navigate anywhere in that paragraph and do it!

(Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse libero sem, posuere id iaculis ac, dignissim eu mauris. Mauris at feugiat augue. Mauris porttitor tempus tincidunt. In enim odio, efficitur nec tempus eget, fermentum non lorem. Sed laoreet faucibus erat, vitae rutrum arcu luctus sed. Duis ultricies pharetra tellus, ac dapibus leo elementum sit amet. Aenean accumsan ultricies orci, ac finibus urna sodales quis. Maecenas iaculis lorem risus, ut commodo eros consequat ut. Suspendisse bibendum vitae massa non consectetur.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse libero sem, posuere id iaculis ac, dignissim eu mauris. Mauris at feugiat augue. Mauris porttitor tempus tincidunt. In enim odio, efficitur nec tempus eget, fermentum non lorem. Sed laoreet faucibus erat, vitae rutrum arcu luctus sed. Duis ultricies pharetra tellus, ac dapibus leo elementum sit amet. Aenean accumsan ultricies orci, ac finibus urna sodales quis. Maecenas iaculis lorem risus, ut commodo eros consequat ut. Suspendisse bibendum vitae massa non consectetur.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse libero sem, posuere id iaculis ac, dignissim eu mauris. Mauris at feugiat augue. Mauris porttitor tempus tincidunt. In enim odio, efficitur nec tempus eget, fermentum non lorem. Sed laoreet faucibus erat, vitae rutrum arcu luctus sed. Duis ultricies pharetra tellus, ac dapibus leo elementum sit amet. Aenean accumsan ultricies orci, ac finibus urna sodales quis. Maecenas iaculis lorem risus, ut commodo eros consequat ut. Suspendisse bibendum vitae massa non consectetur.)

# Visual Mode

Visual mode is nearly as complex! You really don't ever need to use it if you don't like to. Visual mode provides a highlight around your movement actions.

Visual mode MUST be entered when in normal mode.

To enter visual mode press 'v'

Leave visual mode by pressing ESC (going back to normal mode)

## Use any movement keys / actions and see what gets highlighted

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse libero sem, posuere id iaculis ac, dignissim eu mauris. Mauris at feugiat augue. Mauris porttitor tempus tincidunt. In enim odio, efficitur nec tempus eget, fermentum non lorem. Sed laoreet faucibus erat, vitae rutrum arcu luctus sed. Duis ultricies pharetra tellus, ac dapibus leo elementum sit amet. Aenean accumsan ultricies orci, ac finibus urna sodales quis. Maecenas iaculis lorem risus, ut commodo eros consequat ut. Suspendisse bibendum vitae massa non consectetur.

You may yank, cut, or delete anything highlighted

# Command Mode

Command mode is only primarily used to:
- Save your file
- Exit your file
- Jump to a specific line number

You can enter command mode when in normal mode by pressing ':'

You will see a tiny little bar on the bottom of your IDE where you can type!

`:w` - "writes" (saves) your current file
`:q` - "quits" your current file
`:[line number]` - jumps to that specific line number. This is line number 240, jump to line 20, and then back to 240!

# Closing

THAT'S ALL I GOT! WELCOME ABOARD! GOOD LUCK WITH THE ACTIVITY!!

There are tens of more motions + tricks but these are the ones I use on the daily





















Welcome to the bottom of the file! Go back up by typing 'gg' in normal mode and find yourself back