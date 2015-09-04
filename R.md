[RCommander](RCommander)

http://www.ats.ucla.edu/stat/r/seminars/intro.htm

Data Import
----

### Import csv
    read.csv("C:/Tut1Q1Data.csv")

File Management
----

    getwd()
    setwd("C:/work/blah") # note the forward slashes

Data Frames
------

    students <- read.csv("C:/Tut1Q1Data.csv")
    students[1,1]       # first row first column. Note 1 indexed.
    students[1,]        # first row
    students[,1]        # first column
    students[1:10,2:3]  # ranges of rows and columns
    students$Height     # Height column

The type of rows and columns is a `vector`.

Manually construct data frames by creating vectors for each column.

    age <- c(25, 30, 56)
    gender <- c("male", "female", "male")
    weight <- c(160, 110, 220)
    mydata <- data.frame(age,gender,weight)

      age gender weight
    1  25   male    160
    2  30 female    110
    3  56   male    220

Note that R reflects the name of the vectors for the names of the columns in the data frame.

### Column Names

Get column names

    colnames(students)

Change column names via indexing:

    colnames(students)[1] <- "Altitude of head"

Use backticks to escape column names with spaces

    students$`Altitude of head`

### Summarizing

Get dimensions of data frame

    dim(students)

Get summary info about R objects

    str(students)     # structural summary (including types)
    summary(students) # statistical summary

### Subsetting

    subset(students, Weight < 60)

Vectors
---

Create vectors with the `c()` function.

    c(1,2,3,4)

Retrieve non-sequential rows:

    students[c(1,3,5,7,9),]

### Sorting

    sort(v, descending = FALSE)
