TART: A Technical Assignment/Report Template for LaTeX
=======================================================

The TART class was initially written to format lab reports for the ECE 455 and ECE 429 courses at the University of Waterloo, in Waterloo, Ontario. The class was written using MiKTeX, an implementation of TEX for Windows.

How to Use
--------------
Using TART is pretty simple. First, include the TART class by putting `\documentclass{technical_assignment_report}` at the top of your tex file. After this, you can set up your assignment by filling out the following fields:

+ `\coursetitle {<course title>}` sets the course title for the report
+ `\assignmentdate {<date>}` sets the due date of the report.
+ `\assignmenttitle {<assignment title>}` sets the report title.
+ `\groupnumber {<group number>}` sets your group number.
+ `\groupmembers {<name1>}{<name2>}{<name3>}{<name4>}{<name5>}` sets your group members' names, user id numbers, or usernames. You don't need to fill in all the blanks, just make sure there are five sets of braces in all. For reference, see `technical_assignment_report.tex`. 

You're now set! You can now `\begin{document}`.

Setting up a Basic Assignment
------------------------------
Your basic `.tex` file should look something like:

	\documentclass{technical_assignment_report} 

	\coursetitle {ECE 100}
	\assignmentdate {\today}
	\assignmenttitle {Lab \#1 Report}
	\groupnumber {22}
	\groupmembers {jsmith}{r2crusoe}{sholmes}{}{}

	\begin{document}
		\fulltitle
		\brief
		Your brief text.

		\setup %or \environment
		Your setup or environment text.

		\nsection{Some Section Heading}
		Your section text.

		\erroranalysis
		Your error text.

		\ncitation{Results}
		Your results text.
	\end{document}

You have a couple of options with the title. `\fulltitle` currently renders the title with both the group number and the group members. `\fulltitlegroupnum` omits the group members, while `\fulltitlegroupmem` omits the group number.

If the current formatting of the title doesn't suit your needs, you can always just set your `\title` and `\author` the way you would with a normal `.tex` document; `\maketitle` and `\maketitlepage` are still supported.

List of Macros
--------------
### Basic Macros
+ `\course` This displays the full course title as specied above. In this case, it displays ABC 100.
nassignment This displays the assignment title as specifed above. 
+ `\duedate` This displays the due date as specified. 
+ `\group` This displays the group number as specified. 
+ `\groupmem` This displays the groupmembers as specified. Up to 5 are allowed by the definition function. 
+ `\fulltitlegroupnum` This displays the title of the assignment with the course number, assignment title,
date, and group number.
+ `\fulltitlegroupmem` This displays the title of the assignment with the course number, assignment title,
date, and group members.
+ `\fulltitle` This displays the title of the assignment with the course number, assignment title, date,
group number, and group members.

### Section Types
+ `\nsection` This creates a section with supressed numbering.
+ `\ncitation` This creates a section with supressed numbering on a new page. Ideally should be used for citations, results, or glossaries.

### Headings and Default Text Snippets
+ `\brief` Creates a `Brief ' section.
+ `\setup` Creates a `Setup' section.
+ `\environment` Creates an `Environment' section.
+ `\erroranalysis` Creates an `Error Analysis' section.

### Styles
+ `\mnspace` Uses a nice monospace font for code references or numbers.

## Formulae
Some common formulae. Right now this is the only one I could think of to add, but please file an issue if you can think of more commonly used formulae that you'd like to have included.
+ `\percenterror {<differing-num>}{<base-num>}` This displays the the percent error formula.