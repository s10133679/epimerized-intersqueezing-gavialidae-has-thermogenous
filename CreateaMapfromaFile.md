# Introduction #

e.i.g.h.t. now implements a method that allows you to create a map from a file,
currently you are only able to load walls in from this method, Players and Items must be added manually for now( Subject to change in the future ).


# Details #
## How to Format the File ##
  * File must be in the same directory as the project files
  * The first line must consist of two numbers separated with a comma ( eg. 2,3 ),  The first number is the Xsize of the map, the second is Ysize.
  * X increases on the map from left to right, Y increases on the map going down

> `0,0  1,0  2,0`

> `0,1  1,1  2,1`

> `0,2  1,2  2,2`


  * There must be Ysize number of lines after the first line ( described above )
  * Each one of these lines must consist of Xsize number of numbers, separated with commas

## How Some Issues Are Dealt With ##
  * If file is not found, an Exception is thrown and the system will exit with exit code -1
  * In the case that the value is not a number, A  NumberFormatException will be thrown and the system will exit with exit code -1
  * If there are too many X or Y variables in the file they will be ignored
  * If there is not X or Y variables, map will be filled with EMPTY.