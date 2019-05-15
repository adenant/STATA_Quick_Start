# Session 3

## *Intro to loops; Storing results in excel files*

+++

## Loops

- Loops let you automate a LOT of work
- One of the most common ways I use loops is to run a ton of different model specifications
  - Vary over subgroup
  - Vary dependent variable
  - Vary control variables
  - Vary estimation command and options

+++

## Two types of loops

- `forvalues` : loop over numbers
- `Foreach` : loop over anything

+++
## Foreach Syntax

```
foreach <loop control macro> in <list> {

		<commands using loop control macro>

}
```
- Note: another syntax uses “of” instead of “in”
	“in” is the easier syntax


+++
## Forvalues Syntax

```
forvalues <loop control macro> = n(increment)N {

		<commands using loop control macro>

}
```
- Note: n is the starting number, whereas N is the last number

+++
## Loops

- Open the .do file Loop_Demo
- Use  Hands_on_Exercise_data_3

+++
## Storing Results to Excel

- Since Version 14, STATA has the ability to store output to excel file using .putexcel command

- Open Storing_Results_to_Excel_Demo.do

- This .do file used all the things we’ve learnt to export results to excel file for further analyses


