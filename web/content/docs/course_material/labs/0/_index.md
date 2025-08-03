---
title: "Lab 0"
bookHidden: false
marp: false
header: 'CS0.101 Computer Programming (Monsoon 24)'
footer: '![width:150px](IIIT_Hyderabad_Logo.jpg)'
---

# Welcome to CS0.101 Lab 0

https://cpro-iiit.github.io/docs/course_material/labs/0/lab0.pdf

---
## Introduction
Coding can be learnt only by solving programming problems!

80% of the weightage of evaluations is on programming problems.

> __Goal__: Solve 8-9 programming problems every week. 
> (3 in lab, 2 in tutorial, 1-2 in assignment, 2 in practice)
> Solve 100 over the entire course.   

Lab sessions are evaluated (2% marks per lab, 20% for 10 labs).

---
## What's the plan for Lab 0?

1. Help you set up the coding environment.
2. Download problems from AutoLab (https://pingala.iiit.ac.in) and learn the basic tools required for coding.
3. Submitting solutions and seeing the score.
4. Problem-1, Solve a "Hello World" problem.
5. Problem-2, Print "Hello World! I am learning Computer Programming in C, And it is awesome!"
---
## Some Buzz Words!
__AutoLab__: where all labs/assignments problems are set. You can download handouts and upload solutions (or handins). Autolab will automatically grade your solutions and give you a score. You will also get feedback on code from TAs here. You can access autolab in 2 ways.
1. Through the website https://pingala.iiit.ac.in
2. Through autolab commands in the _pingala shell_.

__Pingala Shell__: where you will do all the coding. The _pingala shell_ is a standard Ubuntu Linux shell with all the programs required for this course. This also ensures that the outputs/errors you encounter are similar for the entire batch.


---


## 1. Basic Setup


---


### 1.1 Reseting Password for AutoLab: 
1. Open a browser and go to https://pingala.iiit.ac.in (the web interface for autolab). 
2. Reset your password using forgot password. The username is the IIIT email id. 
3. Goto Outlook Mailbox for instructions for reset.
4. After resetting, login to the site and keep this browser window open, as it is also needed for step 1.3.

>Remember this password! It will be used for all labs, assignments and exams.


---
### 1.2 Open  pingala shell: 

1. Open the Terminal in lab machines and run the command
```bash
ssh <your_iiit_username>@pingala.iiit.ac.in
```
2. Enter your IIIT CAS password to open the _pingala shell_.

_pingala shell_ is a standard Ubuntu Linux shell with all the programs required for this course.

---
### 1.3 Setup AutoLab in the shell: 
1. Run the following command for setting up autolab in _pingala shell_
```bash
autolab setup
```

2. Copy the 6-character access code and paste it into https://pingala.iiit.ac.in/activate in the same browser window where you logged in.
3. More info: https://docs.autolabproject.com/command-line-interface/

---
## 2. Download Problems/Basic Tools for Coding

---
### 2.1 Download Problems
1. Run the  command `autolab courses` to list the courses

2. Run the command `autolab asmts <course_id>` to list the assesments under the courses. <course_id> is "cs0-101-m24" for this course (as shown by the previous command)

3. Run the command `autolab download <course_id>:<asmts_id>` to download the handout for Lab 0. <asmts_id> is "lab0" for Lab 0 (as shown by the previous command)

More Info: https://docs.autolabproject.com/command-line-interface/

---
### 2.2 Navigate folders, edit code, extract/create tar archive in 'pingala shell'

- use `tar xvf <file_name>` to unzip tar archives `tar xvf lab0-handout.tar`. More about tar file: https://en.wikipedia.org/wiki/Tar_(computing)
- use `cd lab0-handout/` and `ls` to check the assessment files (driver.sh, Makefile, p1, p2, README)
- use `nano p1/main.c` to open C file for the lab0/problem-1
  
---
### 2.3 Edit code
- use `nano <file_name>` to edit `<file_name>` as a text file. e.g. `nano p1/main.c`, `nano p2/main.c`
- Edit your code and use `ctrl+o` to write the code. Hit enter to save, and use `ctrl+x` to exit the nano editor. More about nano editor: https://www.nano-editor.org/
- use `cd ..` to exit the current directory
- use `tar cvf <tar_file_name>.tar <folder_name>` to create a tar archive (similar to a zip file) for the folder <folder_name>. e.g. `tar cvf lab0-handin.tar lab0-handout`
- run `ls` to check the created tar files. More Info: https://missing.csail.mit.edu/2020/course-shell/ 

---
### 2.4 Test your solutions locally
- run `make all` to compile both your problem solutions. If it runs inside the problem directory, only that problem is compiled
- run `./main` in each problem directory to see your program running
- run `sh driver.sh` to see your program running on test cases


---
## 3. Submitting Solutions/Seeing Score 

---
### 3.1 Submit solutions
1. go 1 directory above using `cd ..` (now `ls` should show `lab0-handout` directory) and create a tar archive of the entire assessment by running
```tar cvf lab0-handin.tar lab0-handout```
2. submit `l0-handin.tar` using the command
```autolab submit lab0-handin.tar```

---
### 3.2 See your score

- To check your score run
```autolab scores```
- Latest submission score will be consider for grading
- Logout from the pingala shell by running `logout`
- Logout from pingala.iiit.ac.in too

---
## 4. Solve Lab 0

Problem-1: output should be "Hello World!" 

Problem-2: output should be "Hello World!I am learning Computer Programming in C.And it is awesome!"


---
### 4.1 Coding Treasure Hunt!

Use the above clues to solve lab 0 with full marks.

1. Make guesses and try it out.

2. Only when you are completely stuck, ask others.

3. Understand why a guess didn't work out. Read the Error and debug it accordingly.

4. C-error debug: https://naagar.notion.site/C-Error-debug-197096220a264f53a994742fd2d4971d 

---
### Honor Code

> When you copy, you are only damaging yourself!

> When you allow your friend to copy, you are not helping your friend!

> We will run your code for Plagiarism Detection.




---
## Questions
---
### Can I use my computer/editor for coding?
Yes. You can access Autolab through the website (https://pingala.iiit.ac.in) if you are connected to the IIIT network directly or indirectly through VPN (https://vpn.iiit.ac.in/).

Autolab command line could also be installed in Linux systems using directions provided at the links below:  
https://github.com/autolab/autolab-cli   
https://docs.autolabproject.com/command-line-interface/

However, it's recommended to use the __pingala shell__ where everything is already installed. This ensures that you can get help from your colleagues and TAs easily. This is also the same setup used for all exams.

---
### 5.1 Other optional Helpuful shell commands, Delete files/ folders using shell  
- use `rm <file_name>` to delete a file. e.g. `rm p1/main.c`
- use `rm -r <folder_name>` to delete a folder. e.g. `rm -r p1`
- use `-f` flag to delete a file/folder without asking for confirmation. e.g. `rm -f p1/main.c`, `rm -f p1`, `rm -f lab0`
- use `rm -rf <folder_name>` to delete a folder and all its contents. e.g. `rm -rf lab0-handout`
- - use `ls` command to list folders and files in the current directory
- use `cd` to change the directory. e.g. `cd lab0/`
- use arrow keys (up and down) to check the command history. 
---
### 5.2 creating file/folder and copying files/folders using shell
- use `touch <file_name>` to create a file. e.g. `touch p1/main.c`
- use `mkdir <folder_name>` to create a folder. e.g. `mkdir p1`
- use `cp <file_name> <destination_folder_name>` to copy a file to a folder. e.g. `cp p1/main.c p2/`
- use `cp -r <source_folder_name> <destination_folder_name>` to copy a folder to another folder. e.g. `cp -r p1 p2`
---
Happy Programming! 
- Coding is not just a skill, it's an adventure in logic and creativity.
- Writing code is like solving a puzzle, one piece at a time.
- Programming is like playing with Lego bricks, building something amazing from scratch.
  https://scratch.mit.edu/
- Think outside the box, code inside the lines.
---

<p align="center">
  <img src="meme7.jpg" alt="Image 1" width="30%">
  <img src="meme6.png" alt="Image 2" width="30%">
  <img src="meme_0.png" alt="Image 3" width="30%">
  <img src="meme2.jpeg" alt="Image 4" width="30%">
</p>


  
