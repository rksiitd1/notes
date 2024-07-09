# Command Prompt Basics: Essential Syntax Guide

This guide covers fundamental command prompt syntax for Windows. These commands are crucial for navigating the file system, managing files and directories, and performing basic system operations.

## 1. Navigation Commands

### Change Directory (cd)
```
cd [directory]
cd ..         # Move to parent directory
cd /          # Move to root directory
cd %userprofile%  # Move to user's home directory
```

### List Directory Contents (dir)
```
dir
dir /a        # Show hidden files
dir /s        # Show subdirectories
```

### Clear Screen (cls)
```
cls
```

## 2. File and Directory Management

### Make Directory (mkdir)
```
mkdir [directory_name]
```

### Remove Directory (rmdir)
```
rmdir [directory_name]
rmdir /s [directory_name]  # Remove non-empty directory
```

### Copy Files (copy)
```
copy [source] [destination]
copy *.txt C:\backup\      # Copy all .txt files to backup folder
```

### Move Files (move)
```
move [source] [destination]
```

### Delete Files (del)
```
del [filename]
del *.tmp     # Delete all .tmp files
```

### Rename Files (ren)
```
ren [old_name] [new_name]
```

## 3. System Information

### System Information (systeminfo)
```
systeminfo
```

### IP Configuration (ipconfig)
```
ipconfig
ipconfig /all  # Detailed network information
```

## 4. Process Management

### List Running Processes (tasklist)
```
tasklist
```

### Kill a Process (taskkill)
```
taskkill /IM [process_name] /F
```

## 5. File Content

### Display File Content (type)
```
type [filename]
```

### Find Text in Files (findstr)
```
findstr "search_text" [filename]
findstr /s /i "search_text" *.txt  # Search in all .txt files, case-insensitive
```

## 6. Network Commands

### Ping
```
ping [website or IP]
```

### Traceroute (tracert)
```
tracert [website or IP]
```

## 7. Helpful Commands

### Help
```
help
[command_name] /?  # Get help for a specific command
```

### Echo
```
echo [text]
echo %variable%  # Display value of an environment variable
```

## Best Practices

1. Use quotation marks for paths with spaces: `cd "Program Files"`
2. Use up/down arrow keys to navigate command history
3. Use tab for auto-completion of file and directory names
4. Be cautious with delete and move operations; they can't be undone easily

## Tips

- Commands are case-insensitive in Windows
- Use `&` to chain commands: `cd directory & dir`
- Use `|` for piping output: `dir | find "file"`
- Use `>` to redirect output to a file: `ipconfig > network_info.txt`

Remember, these commands are for Windows Command Prompt. PowerShell and Unix-like systems (Linux, macOS) may use different commands or syntax.
