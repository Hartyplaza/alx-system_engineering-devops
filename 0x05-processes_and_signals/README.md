0x05. Processes and signals



About Bash projects

Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.

Resources

Read or watch:

    Linux PID
    Linux process
    Linux signal
    Process management in linux

man or help:

    ps
    pgrep
    pkill
    kill
    exit
    trap

Learning Objectives

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
General

    What is a PID
    What is a process
    How to find a process’ PID
    How to kill a process
    What is a signal
    What are the 2 signals that cannot be ignored

Copyright - Plagiarism

    You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
    You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
    You are not allowed to publish any content of this project.
    Any form of plagiarism is strictly forbidden and will result in removal from the program.



0. What is my PID 
Write a Bash script that displays its own PID.


1. List your processes 
Write a Bash script that displays a list of currently running processes.

Requirements:

    Must show all processes, for all users, including those which might not have a TTY
    Display in a user-oriented format
    Show process hierarchy



2. Show your Bash PID 
Using your previous exercise command, write a Bash script that displays lines containing the bash word, thus allowing you to easily get the PID of your Bash process.

Requirements:

    You cannot use pgrep
    The third line of your script must be # shellcheck disable=SC2009 (for more info about ignoring shellcheck error here)


3. Show your Bash PID made easy 
Write a Bash script that displays the PID, along with the process name, of processes whose name contain the word bash.

Requirements:

    You cannot use ps


4. To infinity and beyond 
Write a Bash script that displays To infinity and beyond indefinitely.

Requirements:

    In between each iteration of the loop, add a sleep 2


5. Don't stop me now! 
We stopped our 4-to_infinity_and_beyond process using ctrl+c in the previous task, there is actually another way to do this.

Write a Bash script that stops 4-to_infinity_and_beyond process.

Requirements:

    You must use kill

Terminal #0


6. Stop me if you can
Write a Bash script that stops 4-to_infinity_and_beyond process.

Requirements:

    You cannot use kill or killall

Terminal #0

I opened 2 terminals in this example, started by running my 4-to_infinity_and_beyond Bash script in terminal #0 and then moved on terminal #1 to run 6-stop_me_if_you_can. We can then see in terminal #0 that my process has been terminated.



7. Highlander 
Write a Bash script that displays:

    To infinity and beyond indefinitely
    With a sleep 2 in between each iteration
    I am invincible!!! when receiving a SIGTERM signal

Make a copy of your 6-stop_me_if_you_can script, name it 67-stop_me_if_you_can, that kills the 7-highlander process instead of the 4-to_infinity_and_beyond one.

Terminal #0

I started 7-highlander in Terminal #0 and then run 67-stop_me_if_you_can in terminal #1, for every iteration we can see I am invincible!!! appearing in terminal #0.

8. Beheaded process 
Write a Bash script that kills the process 7-highlander.

Terminal #0
I started 7-highlander in Terminal #0 and then run 8-beheaded_process in terminal #1 and we can see that the 7-highlander has been killed.
