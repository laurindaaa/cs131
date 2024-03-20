
1. Execute this command :

find /etc -type f > one.txt 2> two.txt

a. Explain in simple English what we are trying to do in this command.
The command "find /etc -type f > one.txt 2 > two.txt" is trying to find all regular files in the "etc" directory and its subdirectories.
It saves the standard output to a file called "one.txt" and saves the standard error to a file called "two.txt".

b. Using the cat command view one.txt and two.txt... In simple English sentences explain your observations about the content found in one.txt and two.txt
"one.txt" contains the all the regular files which found in the "etc" directory and its subdirectories.
"two.txt" contains all error messages encountered during the execution of the command.

------------
2. Which [Month, Year] had the most (top 3) YouTube channels created   [ Use the created year and created month columns ]
Your answer should contain what commands you used along with the output.
Requirement: You should apply cut sort and uniq commands to accomplish this task.
You can use commands in addition to these as well but solve the actual problem using cut sort and uniq.
Example :
As per the Dataset, Top 3 [Month, Year] with the most number of YouTube channels created were :
1. December,2025 with 35 channels
2. December,2060 with 20 channels
3. January,1998 with 16 channels
[ Replace months and years above with your answer ]
The command(s) used to find it was this: _______________
Explain the command along with the parameters used and the reason for using them.

result:
2021,Mar
2020,Jul
2018,May

cmd: cut -d',' -f20,21 'data.csv' | sort -nr | head -3
"cut -d ',' -f20,21 'data.csv'" cut the 20th and 21st columns from the file which 20th column represents the created year,and 21st represents the created month.
"sort -nr | head -3": Sorts the result in descending order, and selects and displays the top 3 lines.
------------
3. Write the command you would use to find all the processes owned by you. Paste the output of the same.
ps -u yelinsp24
    PID TTY          TIME CMD
3528229 ?        00:00:05 systemd
3528231 ?        00:00:00 (sd-pam)
3528237 ?        00:00:01 sshd
3528239 pts/1    00:00:00 bash
3569903 pts/1    00:00:00 ps
------------
4. Open two terminals and login to the IBM VM.
a. In the first terminal execute: vi file.txt Do not quit or close the vi prompt screen at this moment and keep it open.
b. In the second terminal use the same command you used in Q3 and paste the output of it below. What did you notice? What is the Process ID for the vim?
3528229 ?        00:00:05 systemd
3528231 ?        00:00:00 (sd-pam)
3528237 ?        00:00:01 sshd
3528239 pts/1    00:00:00 bash
3570151 pts/1    00:00:00 vim
3570358 ?        00:00:00 sshd
3570359 pts/50   00:00:00 bash
3570403 pts/50   00:00:00 ps

There are more processes and the process ID for vim is 3570151

c. Now go back to the first terminal and quit the vi using: q! option.
d. In the second terminal use the same command you used in Q3 and paste the output of it below. what did you notice? What changed and why?
    PID TTY          TIME CMD
3528229 ?        00:00:05 systemd
3528231 ?        00:00:00 (sd-pam)
3528237 ?        00:00:01 sshd
3528239 pts/1    00:00:00 bash
3570358 ?        00:00:00 sshd
3570359 pts/50   00:00:00 bash
3571321 pts/50   00:00:00 ps

The vim process is gone. Becasue I closed it
------------
5. What is the init process in Linux ? Find the process id for the init process.
Show the command you used to do this. ( Note: The init process is also called systemd in the flavor we use on IBM VM)
pgrep systemd
1
2951
2998
3746
86087
105881
2060795
2073814
2248654
2379540
2422345
2492008
2808486
3304023
3312757
3433756
3491745
3497612
3509567
3511452
3523835
3528229
3533162
3542394
3552870
3558220
3563974
3564958
3570065
3571469
3571480
3571483
3571496
3571506
3854249
init process id is 1
------------
6. Explain the command in not more than 4 sentences:  ps aux
Annotate Assignment2.txt with the Task numbers so the TA can clearly identify your answers. Overall presentation in the text file will be evaluated too.

check the status of all active processes on a system, as well as display detailed technical information about the processes without TTY.

