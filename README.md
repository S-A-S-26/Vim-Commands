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
