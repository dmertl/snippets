Bash & Linux Snippets
=====================

File Manipulation
-----------------

### Slice lines from a file

Slice 1368553 lines from notificationserver.log starting at line 88781976

    tail -n+<start> <file> | head -n<length>
    tail -n+88781976 notificationserver.log | head -n1368553

### Find first line containing string

Find line number of first occurrence of "Nov  4" in notificationserver.log

    grep -n -m 1 "<search>" <file>
    grep -n -m 1 "Nov  4" notificationserver.log 
