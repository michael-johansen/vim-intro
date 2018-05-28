# Intro to vim - a minimalistic presentation

Presenting in vim:

:set cursorline # underline on line with caret
:set showcmd # show current command

View presentation as pdf:

```
markdown presentation.md > presentation.html
wkhtmltopdf presentation.html presentation.pdf 
xdg-open presentation.pdf
```

First draft for this presentation, order of elements might be changed

## Agenda
	[ ] Motivation
	[ ] Modal editing
	[ ] Motions
	[ ] Operators
	[ ] Selection
	[ ] Commands
	[ ] Random tips
	[ ] Resources
	[ ] Workshop

## Motivation 
	[ ] Keyboard centric: Won't break flow
	[ ] Fingers should rest at home row, lowest travel distance
		[ ] Caveat: Optimized for english qwerty-keyboard layout
	[ ] Steep learning curve, but very rewarding

## Modal editing
	[ ] Modes: Normal, insert, command
	[ ] Programming: 90% read, 10% write
	[ ] Workflow: Default to normal mode, with short bursts of insertions, then escape to normal mode
	[ ] Ways to enter normal mode from insert mode or command mode: <ESC> 
	[ ] ProTip: Remap caps-lock to another escape key
```
setxkbmap -layout no -variant nodeadkeys -option caps:escape -option nbsp:none
```
	[ ] Ways to enter insert mode from normal mode
```
i - enter insert mode before caret
a - enter insert mode after caret
I - enter insert mode before line content (before first non-whitespace character)
A - enter insert mode after line content (after last non-whitespace character)
o - enter insert mode on a new line below current line
O - enter insert mode on a new line above current line
```
	[ ] Ways to enter command mode from normal mode <:>

## Do some motions
	[ ] h, j, k, l - Basic navigation. Please do not use arrow-keys
		[ ] ProTip: Increase key-rate for quicker navigation
```
xset r rate 400 50
```
	[ ] H, L - Top/Bottom of screen
	[ ] w, W - until next word/WORD
	[ ] b, B - to previous word/WORD
	[ ] 0, $ - start/end of line 
	[ ] t<target>, until (exclusive) next target character
	[ ] f<target>, until (inclusive) next target character
	[ ] 3w, 2$, 10j - combining a count and a motion
	[ ] gg top, G bottom

## Selection
	[ ] v - visual mode
	[ ] V - visual line mode
	[ ] ^v - visual block mode
		[ ] combine with I to do multiline edit

## Operators combined with motions
	[ ] d - delete
		[ ] D - cursor to end of line
	[ ] c - change
		[ ] C - cursor to end of line
	[ ] y - yank
	[ ] dd, cc, yy, 5dd - operate on whole line(s)
	[ ] d5w, c2$, y2t}, cw - operator [number] motion

## Commands (Know how to quit)

```
:w[rite] [filename] <enter> 	# write
:q[uit][!] <enter> 		# quit, with ! to force
:wq <enter> 			# combine shorthand
:help [topic]			# open help on topic
```
	[ ] u - undo last command (move one step down in changes-stack)
	[ ] ^r - redo last command (move one step up in changes-stack)
	[ ] U - undo all changes on line (added to top of changes-stack, u to undo "undo all")

## Random tips:
```
[ ] Search / %
[ ] Quick search * %
[ ] toggle case ~
[ ] Run terminal commands
[ ] gx - Open url in browser http://www.clave.no 
[ ] Insert mode: ^kOK ✓, ^kXX ✗, :dig[tab]
```

## Resources:
http://www.viemu.com/vi-vim-cheat-sheet.gif

## Workshop

