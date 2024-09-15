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
9. n for next N for previous
## Neo Vim
1. ctrl+w+v to split view
2. space s for opening search
3. ctrl + / to get help while in search
4. ctrl+w+h to go to neotree ctrl+w+l to go to currently open window
5. space w s to search through out workspace
6.  There are several ways to create a terminal buffer:
    Run the :terminal command.
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
7. To show hidden files in neo tree press H.
