1. **Press f and any thing like char or symbol to go to the next one in line ; to repeat the next one and , for previous**
2. **Type d$ to delete to the end of the line.**
3. **To search for a phrase in the backward direction, use ? instead of /.**
4. **Type % to move the cursor to the other matching bracket.**
5. **s/thee/the/g to substitute "new" for "old**
6. To change every occurrence of a character string between two lines, type
  
          :#,#s/old/new/g
  
      where # are the line numbers of the range of lines where the
      substitution is to be done (i.e., 1,3 means from line 1 to line 3, inclusive).
  
      Type
  
          :%s/old/new/g
  
      to change every occurrence in the whole file.
  
      Type
  
          :%s/old/new/gc
  
      to find every occurrence in the whole file, with a prompt whether to
      substitute or not.
7. **Type :! followed by an external command to execute that command**
8. **Use . to repeat the previous command**
9. n for next N for previous.
10. e for end of line.
11. ^ for begging of line which is not an empty string.
12. F to jump backwards followed by the character wherever need to jump.
13. press ma to bookmark the line so i could move back to it using backtick.
## Neo Vim
1. ctrl+w+v to split view
2. space s for opening search
3. ctrl + / to get help while in search
4. ctrl+w+h to go to neotree ctrl+w+l to go to currently open window
5. space w s to search through out workspace
6.  There are several ways to create a terminal buffer:
    Run the :terminal command.
7. In order to add html template type html:5 in inset mode and press ctrl + y in inset mode.
    Call the nvim_open_term() or termopen() function.
    Edit a "term://" buffer. Examples:
    
    :edit term://bash
    :vsplit term://top
    
        Note: To open a "term://" buffer from an autocmd, the autocmd-nested
        modifier is required.
    
    autocmd VimEnter * ++nested split term://sh
    
        (This is only mentioned for reference; use :terminal instead.)
    When the terminal starts, the buffer contents are updated and the buffer is
    named in the form of term://{cwd}//{pid}:{cmd}. This naming scheme is used
    by :mksession to restore a terminal buffer (by restarting the {cmd}).
    The terminal environment is initialized as in jobstart-env.
8. To show hidden files in neo tree press H.
9. install `sudo apt install ripgrep` in order for live grep to work.
10. gd to jump to defination of a function.
11. press '`' to move between the previous and current line.
12. press space+ca to auto import things if it shows not imported on them.
13. To check current file name press 1 Ctrl + G.
14. Second way to get current file name !ls %:p in command line.
           ``` :! - This runs an external shell command (in this case, ls) from within NeoVim.
            ls - This is the shell command to list files in a directory.
            % - This represents the current file in the buffer (the file you are currently editing).
            :p - This modifier turns the current file (%) into its full path   ```   
15. Surround word with whatever is needed with ysiw then b for bracket," for quote.
16. use :mksesssion nameoffile to save session and :source nameoffile to load session.
17.     Old text                    Command         New text
--------------------------------------------------------------------------------
    surr*ound_words             ysiw)           (surround_words)
    *make strings               ys$"            "make strings"  from the pointer to the end of line add string
    [delete ar*ound me!]        ds]             delete around me!
    remove <b>HTML t*ags</b>    dst             remove HTML tags
    'change quot*es'            cs'"            "change quotes"
    <b>or tag* types</b>        csth1<CR>       <h1>or tag types</h1>
    delete(functi*on calls)     dsf             function calls
