# Intro to vim - a minimalistic presentation

[ ] Agenda
	- Motivation
	- Navigation
	- Modal editing
	- Commands
	- Motions
	- Workshop

[ ] Motivation
	- Keyboard centric: Won't break flow
	- Fingers should rest at home row, lowest travel distance
		- Caveat: Optimized for english qwerty-keyboard layout

[ ] Modal editing
	- Modes: Normal, insert, command
	- Programming: 90% read, 10% write
	- Workflow: Default to normal mode, with short bursts of insertions, then escape to normal mode
	- Ways to enter insert mode
```vim
i - enter insert mode before caret
a - enter insert mode after caret
I - enter insert mode before line content (before first non-whitespace character)
A - enter insert mode after line content (after last non-whitespace character)
o - enter insert mode on a new line below current line
O - enter insert mode on a new line above current line
```

[ ] Commands
	- Basic commands
```vim
:w[rite] [filename] 	# write
:q[uit][!] 		# quit, with ! to force
:wq 			# combine shorthand
```

Random:
:set cursorline # underline on line with caret
