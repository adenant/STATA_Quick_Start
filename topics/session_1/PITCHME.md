# Sesi 1
## *Pengantar Pemrograman Statistik, Pengenalan STATA, dan Sintaksis Perintah dalam STATA*

+++

## Introduction
- There’s a lot more to actually doing statistics than just running the analyses and tests
- Many statistical analysis software have a LOT of pre-packaged routines to run regressions, probits, instrumental variables, random effects, zero-inflated negative binomial models….
- Given the computing power of modern computers, these analyses may only take seconds (depending on how large the datasets is)
- Before you can use those commands, your data need to be ready
    
+++

## Introduction
- Your data will NEVER come in a ready-to-use form
- You could prepare the data in Excel with a lot of copying and pasting
    - Time consuming
    - Hard to document
    - If anything changes, you have to start from scratch
- MUCH better to learn how to program!

+++
## Why statistical programming?

- Efficiency: Automate routine tasks and let the computer do them over and over again for you
- Power: Do things that aren’t part of the package (data manipulation, custom functions, etc.)
- Documentation: Keep all notes on what have been done on data manipulations and analyses
- Modification: Allow for performing changes, adjustment, modification, without the need to do the whole routine all over again

+++

## Why Stata?

- Has a LOT of pre-packaged routines to perform many data manipulations and analyses
- Relatively easy to learn (has pull-down menu and command bar)
- Has the facility to do programming
- and many more

+++

## Introduction to STATA

- STATA comes in several different flavors
    - The grown-up versions of STATA are
        - STATA SE (fully equipped STATA)
        - STATA MP (fully equipped and designed to use multiple processors)
    - The impaired versions are
        - STATA IC (like SE, but with built in limits)
        - Small STATA

+++

## Introduction to STATA

- Let’s open STATA
    - Upper-middle: the results window, where STATA communicates to you
    - Bottom: the command bar, where you communicate to STATA
    - Upper-left: the review window, where you see what you just typed
    - Lower-left: the variables window, where you see information about your dataset
    - Right: Variable properties window, where you see information about the variable


+++

## Introduction to STATA

- Let’s open a made-up dataset about pharmacies
    - Hands_on_Exercise data_1
- The sample has 25 fictional pharmacies
- Notice that the command shows up in the Review window
- Variables now show up in the Variables window


+++

## Introduction to STATA

- In addition, STATA has 3 very useful windows that open as separate windows
- Open them from the Window menu
    - Do-file window: where you’ll write programs (we’ll do that one later)
    - Viewer: where you access documentation (also for later)
    - The Data Editor, where you can see the data

+++

## STATA Command Line

- OK, now let’s do stuff
- Most STATA commands follow the same basic syntax
- You pretty much always have a command name and a list of variables
    -`.summarize ZeroFillPre`
- Then you can expand the command with lots of options

+++

## STATA Command Line

- Structure of STATA command line:
    - Pre-colon stuff `:`
    - Command name
    - Varlists
    - if, in, weights
    - `,` post-comma options
- Example:
    - `. sort Treated`
    - `. by Treated: sum ZeroFillPre if Chain==“Yes” , detail`
    
+++

## STATA Command Line

- Pre-colon options:
    - `by <varlist> :` repeats the command for different subgroups, defined by <varlist>
        - The data must be sorted by <varlist>
    - `svy:` tells STATA to adjust for survey features (we’ll cover this later)
    - Some other features require specification before the colon
    - Pre-colon options aren’t used very often

+++

## STATA Command Line

- Varlists:
    - Some commands take multiple variables
    - For some commands, the order of the variables matters
        - Example: regress
    - For others, the order doesn’t matter
        - Example: drop, keep, summarize

+++

## STATA Command Line

- AFTER the varlists but BEFORE the (optional) comma: if/in/weight
- BY FAR the most common is “if”
- “if” applies the command only to variables that meet some condition
- Examples:
    - `.sum ZeroFillPost if Chain == “Yes”`
    - `.sum ZeroFillPost if ZeroFillPre > 0.6`
    - `.sum ZeroFillPost if prov_cnty_cd != 01`

+++

## STATA Command Line

- Operators:
    - Logical: `&    |    !     ~`
    - Relational:  `>   <     >=      <=    ==    !=      ~=`
- NOTE WELL: you need TWO equal signs == to test equality
- Single equal signs = are reserved for assigning values

+++

## STATA Command Line

 
- `in:` applies the operation to specified range of observations
    - `. sum ZeroFillPre in 1/10`
    - `. sum ZeroFillPre in -11/-2`
- VERY rarely used

+++

## STATA Command Line

- Weights are also specified before the comma
- Very important when dealing with survey data
- We will not cover this in this workshop

+++

## STATA Command Line

- Most commands have a huge number of potential options that you can apply
- These are specified AFTER a comma
- These are specific to the command
- How do you learn what options are available for a given command? Example:
    - `. help sum`
    - `. help table`
- Documentation manuals have more detail

+++

## STATA Command Line

- Let’s try out some STATA commands
- Open “STATA Basic Commands Exercise.docx”
- Try to accomplish the specified tasks; hints are in “(…)

