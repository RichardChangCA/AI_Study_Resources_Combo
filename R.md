1. W3Schools R Tutorial: https://www.w3schools.com/r/r_intro.asp

R is often used for statistical computing and graphical presentation to analyze and visualize data.

paste(): concatenate, or join, two or more elements, uses comma(,), cannot combine a string and a number, merge two strings

Type conversion: as.numeric(), as.integer(), as.complex()

Math: ceiling(), floor(), abs()

cat() function for the string: line breaks to be inserted at the same position as in the code.

nchar() function to find the number of characters in a string.

grepl() function to check if a character or a sequence of characters are present in a string

Arithmetic operator %% : Modulus(Remainder from division) or Integer Division.

x <- 1 or 1 -> x , both of them work

R Miscellaneous Operators:
: Creates s series of numbers in a sequence x <- 1:10
%in% Find out if an element belongs to a vector x %in% y
%*% Matrix Multiplication x <- Matrix1 %*% Matrix2

next statement: skip n iteration without terminating the loop(similar as continue for other programming languages)

Global variables: variables that are created outside of a function. can be used by everyone, both inside of functions and outside. Operator: <<-

Vectors: c() function, separate the items by a comma. length() to calculate vector length, negative index numbers to access all items except the ones specified.

rep(): repeat vectors for each value, repeat the sequence of the vector, repeat each value independently

seq(): to make bigger or smaller steps in a sequence for generating sequenced vectors, from, to, by.

list(): A list in R can contain many different data types insdie it, a list is a collection of data which is ordered and changeable.

cbind() function to add additional columns in a Matrix, rbind() for rows, can also combine two matrices

dim() function to find the amount of rows and columns in a Matrix

arrays can have more than two dimensions, arrays can only have one data type

data.frame() are data displayed in a format as a table, data frames can have different types of data inside it, but each column should have the same type of data. summary(0 function to summarize the data from a data frame. 

facors() are used to categorize data, levels() is the set of factors

multiple lines: plot() together with lines()

To compare the plot with another plot, use the points() function

which.max(), which.min() functions to find the index position of the max and min value in the table

2. RStudio global 2021 Conference Notes:

RStudio Package Manager: https://rstudio.com/products/package-manager/

Twitter of RStudio::global(2021) https://twitter.com/search?q=%23rstudioglobal

All conference videos are recorded at https://rstudio.com/resources/webinars/

Reports with R Markdown: Reporducible, Dynamic, Multiple output formats
Step1: Find your brand(font, color, etc.)
Step2: Build a template
Step3: Polish(e.g. ggplots themes)
Package: ratlas, Github: https://github.com/atlas-aai/ratlas
Other R markdown examples: sorensonimpact, thesisdown, rticles

Shiny bindCache() functoin: will cache all previous values(as long as they fit in the cache) and they can be shared across user sessions.
https://rdrr.io/github/rstudio/shiny/man/bindCache.html
Caching details:
Size: Default cache size is 200MB in memeory. Size can be changed and cache can be stroed on disk.
Scope: Cache is shared across all user sessions of the app. Can be scoped just to one session.
Lifetime: A memory cache is discarded when the app exits or restarts. But a disk-based cache can persist across app restarts, and can be shared among multiple processes with Coneect or Shiny Server Pro.

One of the foundations of cognitive behavioral therapy:
I must be a moron if I cannot perform this simple maintenance task.
-This is not something I do very often so it is unreasonable to expect that I would automatically be expert at it.
The documentation is useless and does not help me at all.
-It is not possible to document every possible existing situation; but I can still read the docs and learn something.
This was a total waste of time. I will never get those 4 hours back again.
-Maybe  I did not succeed in my original goal, but I made some progress, and I gained valuable insights for the next time I try.

Custom themes in Shiny & R Markdown with {bslib} & {thematic}
https://talks.cpsievert.me/20201215/rstudio-global.pdf

R-Universe: https://r-universe.dev/organizations/
R ecosystem, a tool to monitor the quality, health, and impact of R packages.
R-Universe is an open platform, where we will experiment with showing metrics and other background information about packages, that may reveal something about the health and the impact of the project, and also facilitate discovery of other software.







