# myls

A short program which behaves like the well-known "ls".

## Description of the project

### Summary

`myls [-laRA] [file ...]`

### Description of the options

-l

(The lowercase letter "ell".)  List in long format.
The following information is displayed for each file: file type, file mode, number of hard links, owner name and group name if any, number of bytes in the file, abbreviated month, day-of-month file was last modified, hour file last modified, minute file last modified.
If the output is to a terminal, a total sum for all the file sizes is output on a line before the long listing.

-a

Include directory entries whose names begin with a dot (.).

-R

Recursively list subdirectories encountered.

-A

List all entries except for '.' and '..'.

Furthemore, these options can be combined with each other (the 'a' option prevails over the 'A'), as in :

```
myls -la
myls -l -A
myls -ARal
myls -alRA
```

## Constraints

This small project had to be implemented in **Ansi C**, using a small set of functions:

- malloc(3)
- free(3)
- exit(3) 
- assert(3)
- opendir(3)
- readdir(3)
- closedir(3)
- chdir(2)  
- stat(2)  
- lstat(2)  
- getpwuid(3) 
- getgrgid(3)  
- strftime(3)
- getenv(3) 
- isatty(3)
- perror(3)
- readlink(2)
- write(2) 
- localtime(3)

Global and non constant static variables are strictly prohibited.
