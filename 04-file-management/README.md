# File Management in Linux

## File and Directory Operations

```bash
1. ls                             # List files and directories in the current directory
2. cd /path/to/dir                # Change the current working directory
3. pwd                            # Print current directory path
4. mkdir new_folder               # Create a new directory
5. mkdir -p a/b/c                 # Create nested directories
6. rmdir empty_folder             # Remove an empty directory
7. rm file.txt                    # Delete a file
8. rm -r folder                   # Recursively delete a folder and its contents
9. cp file1.txt file2.txt         # Copy a file to another
10. cp -r dir1 dir2               # Recursively copy a directory
11. mv old_name new_name          # Rename or move a file/directory
12. touch newfile.txt             # Create an empty file
13. file file.txt                 # Identify the type of a file
14. stat file.txt                 # Show detailed info (size, access time, etc.)
15. tree                          # Display directory structure in tree format
```

## Viewing and Editing Files

```bash
16. cat file.txt                  # Display the contents of a file
17. tac file.txt                  # Display the contents in reverse order
18. less file.txt                 # View file with scroll support (forward/backward)
19. more file.txt                 # View file one page at a time (forward only)
20. head -n 10 file.txt           # Show first 10 lines of a file
21. tail -n 10 file.txt           # Show last 10 lines of a file
22. nano file.txt                 # Open file in nano text editor
23. vi file.txt                   # Open file in vi editor
24. echo 'Hello' > file.txt       # Write text to a file (overwrite)
25. echo 'World' >> file.txt      # Append text to a file
26. cat > file.txt                # Write to file from stdin (Ctrl+D to end)
27. cat >> file.txt               # Append to file from stdin (Ctrl+D to end)
28. diff file1.txt file2.txt      # Show line-by-line difference between two files
29. wc -l file.txt                # Count the number of lines in a file
30. wc -w file.txt                # Count the number of words in a file
31. wc -c file.txt                # Count the number of bytes in a file
```
