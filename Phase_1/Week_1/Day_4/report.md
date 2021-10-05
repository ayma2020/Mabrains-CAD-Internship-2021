# vim Text Editor Tutorial
### If we connect on Linux machine on cloud like Amazon, then GUI text editor like gedit will not be available so vim is the premier text editor for Linux.
---
#### Open txt file using vi
![launch_vi](https://user-images.githubusercontent.com/91392322/135931481-b1565a3d-301a-4315-b443-029ffca2cfbf.PNG)
---
#### Command/Normal Mode
Command mode is used to move around a document, manipulate text(copy-cut-paste-change), and access the other two modes(insert,ex). 
to come back from any mode to this mode, press "esc".
![Commmand_mode](https://user-images.githubusercontent.com/91392322/135931720-3bea3387-692e-4112-b6bd-70464313014f.PNG)

* Movements
  * **G** to move to the last line of the file 
  * **gg** to move to the first line of the file
  * **5G** to move to the fifth line of the file
  * **^** to move to the beginning of a line 
  * **$** to move to the end of a line 
  * **ctrl,G** to tell you where cursor is.
  ---
* Searching (latteral text and RE)
  * /word_you_want_to_search_first_match_after_current_cursor
  * ?backword_search_first_match_before_current_cursor
  * **n** the next matched word
  * **N** the preiveous matched word
  ---
* Undo
  * **u** to undo the last change
  ---
* Delete = Cut, delete from the current file and save at buffer=clipboard
  * **dd** cut the whole current line on cursor. delete even if empty line
  * **d$** cut line from the cursor to the end but do not delete empty line
  * **d3d** or **3dd** cut the next 3 lines
  * **dw** cut word
  * **dh** cut character before the cursor
  ---
* Yank = copy, a clone to buffer
  * **yy** copy the current line on cursor
  * **y3y** or **3dd** copy the next 3 lines
  * **yw** copy word
  * **yh** copy character before the cursor
  * **y$** copy line from cursor to the end
  ---
* Put = paste
  * **p** paste after cusror
  * **P** paste before cursor
  ---
* Change , cut and will open insert mode so we can write text in the place of cut, looks like replace. so change as name is mnemonic
   * **cc** change the current line on cursor
  * **c3c** or **3dd** change the next 3 lines
  * **cw** change word
  * **ch** change character before the cursor
  * **c$** cohange line from cursor to the end
---
#### Insert Mode

To add text to the document, we'll enter **insert mode**.
* **i** to add text before the cursor
* **a** to add text after the cursor
* **A** to add text at the end of the line
* **I**	to add text at the beginning of the line
* **o**	to add text on a blank line after the cursor
* **O**	to add text on a blank line before the cursor
---
#### Ex Mode
![insert_mode](https://user-images.githubusercontent.com/91392322/136043064-16d5c667-b304-471e-a3bc-2e27ad6e1945.PNG)

We can go to **Ex mode** by pressing ':' then we can write file-related commands like opening, saving or aborting changes to a file.
* **:w** to save changes
* **:q** to quit if we did not do any changes, but if there is changes, we must use :w save first before quit
* **wq** to save and quit
* **:q!** to quit without saving changes
---
* Note
  some jobs or functions can be done by insert or normal mode, like going to line number 10G or :10
  ,like wq save(write) and quit ZZ 
