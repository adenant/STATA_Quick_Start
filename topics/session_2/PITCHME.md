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



