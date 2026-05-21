-> zuhaib_khan@DESKTOP-KE4EHHC:~$ touch notes.txt
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ cat notes.txt
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ echo "Hi i am learning devops" >> notes.txt
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ cat notes.txt
Hi i am learning devops
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ echo "I am learning it it 90 days" >> notes.txt
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ echo "I am currently doing Btech CSE ">> notes.txt
->zuhaib_khan@DESKTOP-KE4EHHC:~$ echo "I am practicing linux"| tee -a notes.txt
I am practicing linux
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ cat notes.txt
Hi i am learning devops
I am learning it it 90 days
I am currently doing Btech CSE
I am practicing linux
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ head -n 2 notes.txt
Hi i am learning devops
I am learning it it 90 days
-> zuhaib_khan@DESKTOP-KE4EHHC:~$ tail -n 2 notes.txt
I am currently doing Btech CSE
I am practicing linux
zuhaib_khan@DESKTOP-KE4EHHC:~$



















