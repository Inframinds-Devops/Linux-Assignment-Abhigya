## Task 1

* Create a file with your firstname
* Add few lines to the file without using text editor
* Add few more lines to the file without using text editor
* Rename the file with your lastname
* Print first 5 lines of the file
* Print last 5 lines of the file
* Print lines 2 to 6, don't use sed

### Steps

* `touch Abhigya`
* `echo "Test Line" >> Abhigya`
* `echo "Test 2" > Abhigya`
* `mv Abhigya Krishna`
* `head -5 Abhigya`
* `tail -5 Krishna`
* `head -6 Abhigya | tail -5`


## Task 2

* Create a file with first name in text editor, don't close the text editor
* Create a file with last name in text editor, don't close the text editor
* List out processes running in a system
* Kill the process belonging to file with first name being opened in text editor

### Steps

* Open a terminal, type `nvim Test1` and type something.
* Open another terminal, type `nvim Test2` and type something.
* Open a third terminal, use `htop` and press `f3` to find the `nvim` process.
* Use `kill <pid>` to kill the process.
