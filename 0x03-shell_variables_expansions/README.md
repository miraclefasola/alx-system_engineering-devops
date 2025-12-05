# 0x03. Shell, init files, variables and expansions

## Task 0: <0-alias>
Create a script that creates an alias.

- **Name:** `ls`  
- **Value:** `rm *`

### Example

```bash
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 

⚠️ Warning: This alias is destructive because running ls after sourcing the script will delete all files in the current directory. Use \ls to bypass the alias and list files normally.

# 0x03. Shell, init files, variables and expansions

This project introduces shell initialization files, variables, aliases, and expansions in Linux.

---

## Task 0: <0-alias>
Create a script that creates an alias.

- **Name:** `ls`  
- **Value:** `rm *`

### Example
```bash
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 

## Task 2: <2-path>
Add `/action` to the `PATH`. `/action` should be the last directory the shell looks into when searching for a program.

### Example
```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action

## Task 3: <3-paths>
Create a script that counts the number of directories in the `PATH`.

### Example
```bash
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ . ./3-paths
11
julien@ubuntu:/tmp/0x03$ PATH=/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:::::/hello
julien@ubuntu:/tmp/0x03$ . ./3-paths
12
