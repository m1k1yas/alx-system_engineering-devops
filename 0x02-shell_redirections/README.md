# Shell, I/O Redirections and filters
## About Bash Projects
**0. Hello World**
prints “Hello, World”, followed by a new line to the standard output
```bash
echo "Hello, World"
```

**1. Confused smiley**
displays a confused smiley "(Ôo)'
```bash
echo "\"(Ôo)'"
```

**2. Let's display a file**
Display the content of the /etc/passwd file
```bash
cat /etc/passwd
```

**3. What about 2?**
Display the content of /etc/passwd and /etc/hosts
```bash
cat /etc/passwd /etc/hosts
```

**4. Last lines of a file**
Display the last 10 lines of /etc/passwd
```bash
tail -n 10 /etc/passwd
```

**5. I'd prefer the first ones actually**
Display the first 10 lines of /etc/passwd
```bash
head /etc/passwd 
```

**6. Line #2
Displays the third line of the file iacta working directory**
```bash
head -3 iacta | tail -1 
```

**7. It is a good file that cuts iron without making a noise**
Creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line
```bash
echo "Best School" > \\\*\\\\"'\"Best School\"\\'\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)
```

**8. Save current state of directory**
Writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it
```bash
ls -la > ls_cwd_content
```

**9. Duplicate last line**
Duplicates the last line of the file iacta
```bash
tail -1 iacta >> iacta
```

**10. No more javascript**
Deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders
```bash
find . -name "*.js" -type f -delete
```

**11. Don't just count your directories, make your directories count**
Counts the number of directories and sub-directories in the current directory
```bash
find . -mindepth 1 -type d | wc -l
```

**12. What’s new**
displays the 10 newest files in the current directory
```bash
ls -t | head -n 10
```
**13. Being unique is better than being perfect**
Takes a list of words as input and prints only words that appear exactly once
```bash
sort | uniq -u
```

**14. It must be in that file**
Display lines containing the pattern “root” from the file /etc/passwd
```bash
grep "^root" /etc/passwd
```

**15. Count that word**
Display the number of lines that contain the pattern “bin” in the file /etc/passwd
```bash
grep -c "bin" /etc/passwd
```

**16. What's next?**
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd
```bash
grep -A3 root /etc/passwd
```

**17. I hate bins**
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”
```bash
grep -v "bin" /etc/passwd
```

**18. Letters only please**
Display all lines of the file /etc/ssh/sshd_config starting with a letter
```bash
grep  "^[a-zA-Z]"  /etc/ssh/sshd_config
```

**19. A to Z**
Replace all characters A and c from input to Z and e respectively
```bash
tr 'Ac' 'Ze'
```

**20. Without C, you would live in hiago**
Create a script that removes all letters c and C from input
```bash
tr -d 'Cc'
```

**21. esreveR**
Write a script that reverse its input
```bash
rev
```

**22. DJ Cut Killer**
displays all users and their home directories, sorted by users based on the the /etc/passwd file
```bash
cat /etc/passwd | cut -d: -f1,6 | sort
```
