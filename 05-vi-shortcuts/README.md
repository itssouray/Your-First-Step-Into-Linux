# VI Editor Shortcuts

## 1. Modes in VI Editor
- **Normal Mode** (default) – Used for navigation and command execution.
- **Insert Mode** – Used for text editing (`i` to enter, `Esc` to exit).
- **Command Mode** – Used for saving, quitting, searching (`:` to enter from Normal mode).

---

## 2. Basic Navigation

```bash
1. h               # Move left  
2. l               # Move right  
3. j               # Move down  
4. k               # Move up  
5. 0               # Move to beginning of the line  
6. ^               # Move to first non-blank character  
7. $               # Move to end of the line  
8. w               # Move to next word  
9. b               # Move to previous word  
10. gg             # Go to beginning of file  
11. G              # Go to end of file  
12. :n             # Go to line number n  
13. H              # Move to top of the screen  
14. M              # Move to middle of the screen  
15. L              # Move to bottom of the screen  
```

---

## 3. Insert Mode Shortcuts

```bash
16. i              # Insert before cursor  
17. I              # Insert at beginning of line  
18. a              # Append after cursor  
19. A              # Append at end of line  
20. o              # Open new line below  
21. O              # Open new line above  
22. Esc            # Exit insert mode  
```

---

## 4. Editing Text

```bash
23. x              # Delete character under cursor  
24. X              # Delete character before cursor  
25. dw             # Delete a word  
26. dd             # Delete current line  
27. d$             # Delete from cursor to end of line  
28. d0             # Delete from cursor to beginning of line  
29. D              # Delete to end of line  
30. u              # Undo last action  
31. Ctrl + r       # Redo last undo  
32. yy             # Yank (copy) current line  
33. yw             # Yank a word  
34. p              # Paste after cursor  
35. P              # Paste before cursor  
36. >>             # Indent line  
37. <<             # Unindent line  
38. J              # Join the current line with the next  
```

---

## 5. Search and Replace

```bash
39. /pattern       # Search forward for 'pattern'  
40. ?pattern       # Search backward for 'pattern'  
41. n              # Repeat last search forward  
42. N              # Repeat last search backward  
43. :%s/old/new/g  # Replace all occurrences in file  
44. :s/old/new/g   # Replace all occurrences in current line  
45. :%s/old/new/gc # Confirm each substitution  
```

---

## 6. Working with Files

```bash
46. :e filename        # Open a new file  
47. :w                 # Save file  
48. :wq                # Save and exit  
49. :q!                # Quit without saving  
50. :x                 # Save and exit (same as :wq)  
51. ZZ                 # Save and exit (shortcut)  
```

---

## 7. Working with Multiple Files

```bash
52. :split filename    # Split horizontally and open file  
53. :vsplit filename   # Split vertically and open file  
54. Ctrl + w + w       # Switch between split panes  
55. Ctrl + w + q       # Close current split window  
56. Ctrl + w + s       # Split current window horizontally  
57. Ctrl + w + v       # Split current window vertically  
```
