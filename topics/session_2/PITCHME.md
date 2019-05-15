# Session 2

## *Intro to DO file and macro*

+++

## Do Files [U 16]

- A “program” in STATA is called a “do file”
- A do file is a text file that contains a bunch of STATA commands
- When you run the do file, it executes the commands
- To work with do files, you use the do file editor

+++

# Do Files

- To work with do files:
  - From STATA’s window menu, select Do File Editor
  - Within the do file editor, you can
     - Open existing do files
     - Write a new do file
     - Save your do file
     - Run your do file

+++

# Do Files

- NOTE WELL: you CANNOT open do files directly from STATA or by clicking on the file; you MUST be in the do file editor!!!!!!

+++

# Do Files

- Example: let’s write the words “Hello World” on the screen
- Use the “display” command
- Display can do two things:
  - Print text to the screen (use quotes)
  - Turn STATA into a glorified calculator (don’t use quotes)
- Example:
  - `. disp 2+2` or `. disp “2+2”`
  
+++

# Do Files

- We want to print the line “Hello World”
- Do we need to use quotes or not?
  - `. disp “Hello World”`
- Now write a code in a .do file and execute it to print the line “Hello World”

+++

# Do Files

- You should do everything in do files
- Principles of Do File writing
  - Write for the future
  - Write for other audiences
  - Write to catch mistakes
  - Write to not know what’s going on
  - Write to change your mind

+++

# Do Files
- Principles of Do File writing (cont.)
  - Don’t repeat yourself
  - If you modify data, save to new file
- Reminder: SAVE BACKUPS OF EVERYTHING! BACKUP EARLY AND OFTEN!!!!!!!!

+++

# Do Files

- Write for the future
  - You will be coming back to this program later
  - STATA may have changed
    - Use Version control
  - You will have forgotten what you were thinking
    - Comment
    
+++

# Do Files

- Comments
  - `/*     */`: Useful for commenting out whole blocks of code
  - `//`: For general comments
  - `///`: Kills the line break, so you can write long lines; and must precede with a space
  - `*` : Also comments out rest of the line; I often use ********* to denote “section” breaks in my code

+++

# Do Files

- Begin with a short note about the purpose of the do file
- Specify the condition that the program should be in when you start

+++

# Do Files

- Each dataset should be created without altering the original data
- The program saves the modified data to a different file
- The program loads its own data instead of relying on data being in memory
    - Helps documentation
    - Helps you know what to assume is in memory
    - This also makes debugging a LOT easier
    - Doesn’t apply to do files called by other do files

+++

# Do Files

- Write to change your mind
- DON’T “hard code” values in the middle of your code
- Where practical, have STATA discover values (like the maximum value of something)
- Where that’s not practical, declare a local macro at the TOP of the do file
- If you need to really build in an assumption, comment in a warning about it

+++

# Do Files

- EVERY time you repeat yourself, you create room to make mistakes
  - Forget to change something
- One life saver: looping Instead of copying the same command 7 times, with minor changes, write a loop
- You type the line ONCE, and tell STATA to run it 7 times
- You specify what changes

+++

# Do Files

- Good practice: if a do file alters the data, it saves the altered data to a new dataset with a different name
- STATA opens the dataset it uses
- STATA saves its output
- Problem: where does STATA find/save the data?
  - Specify current working directory
  
  +++

# Do Files

- Use “Change Working Directory” under File to locate the folder where your DATA are located
- This doesn’t need to be the same place as your do file, but any “helper” do files must be in the same place
   - `. use Lecture2_2013_09_13.dta"` 
- Alternatively, specify the working directory in the .do file using .cd command

  +++

# Do Files

- useful tip: to have STATA run its entire program without pausing every screen:
  - `. set more off`
  
+++

# Macros

- The heart and soul of programming in STATA is the local macro
- In most programming languages, these would be called “local variables”
- In STATA, variable refers to the data, so we call them “local macros” or “locals”

+++

# Macros

- To use a macro
  - Type `<macro name>’
  - NOTE WELL: the left-hand slashy thing is NOT an apostrophe, but the thing under the tilde on the upper left-hand side of the keyboard
```
    . local Fred = 2+2
    . disp `Fred’
```




