## Cyber Security Lab 2: Set-UID Program lab 

### Task 1-2 
There is no difference from the child process to the parent process in terms of \n
variables available. the diff command read no difference besides the composed files names.

### Task 3
it appears the environ variable is what stores seemingly all the environment variables when it pertains to the Systems Environment variables.

### Task 4 
I ran the command and as expected the data came out running the usr/bin/env data content.

### Task 5
I ran the command and it looks like a lot of variables have been excluded namely the lessOpen and User and SSH variables. I take it this child process being it was forked won't allow global variables or root environment variables to be printed. 

## Task 6
This got spooky... without calling the proper ls bin function being it was privileged by the root and the root group had access to it the system command didn't need a direct path, but a relative path... which is spooky if someone is just trying to read your data maliciously. 

## Task 7 
When running in root user it ran and slept but for all attempts not given access to the newlycreated program it would need to have the variable exported to run the program in the libmylib.so.1.0.1 file
 
## Task 8
I was able to run the program and i was able to modify the integrity of the call due to the fact all i need to do is run a true cat to the file i want but after i can throw a sneaky && in there and do whatever i want with root access since this is a priveliged program. I just did something basic like "./catall file2 && ls" but that was enough to print my info and then show me the files available in that directory. I can imagine if i wanted to i could hit the method with a "./catall /usr/bin/env && cd / && rm -rf" which would be extremely hazardous. 

The attacks in step 1 still worked even with execve because the program was privileged. 

