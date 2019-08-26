# Coding Dojo 
This project gives a tutorial for a Coding Dojo.
- A Coding Dojo is a meeting where a bunch of coders get together to work on a programming challenge.
- Engage in Deliberate Practice: seek out experiences that will stretch your skills just the right amount, and give you feedback that enables you to learn
- "No master ever stops learning"
- Have fun!

## The Rules
- It is a design training place: "the code is the design"
	- Code without tests simply doesn't exist
- Explain what you do and share what you learned
- Slow down. If you know how to do it: Teach! don't be bored

## How?
- Two people at the keyboard solving the Kata together, one driving the keyboard, the co-pilot instructing the driver
- Start from scratch
- Use TDD and Babysteps
- Everyone follows what is going on and can make helpful suggestions
- The pair at the keyboard explains what they are doing

# The Challenge: A String Calculator

## Challenge Part 1:
Create a simple String calculator with a method
~~~~
int Add(string numbers)
~~~~
- The method can take 0, 1 or 2 numbers, and will return their sum (for an empty string it will return 0) for example: "" or "1" or "1,2"
- The separator between numbers is a comma ","
- Start with the simplest test case of an empty string and move to 1 and two numbers
- Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
- Remember to refactor after each passing test

## Challenge Part 2:
- Allow the Add method to handle an unknown amount of numbers

## Challenge Part 3:
- Allow the Add method to handle new lines between numbers (instead of commas).
	- the following input is ok:  "1\n2,3"  (will equal 6)
	- the following input is NOT ok:  "1,\n" (not need to prove it - just clarifying)

## Challenge Part 4:
- Support different delimiters to change a delimiter, the beginning of the string will contain a separate line that looks like this:   "//[delimiter]\n[numbers…]" for example "//;\n1;2" should return three where the default delimiter is ‘;' .
	- the first line is optional. all existing scenarios should still be supported

## Challenge Part 5:
- Calling Add with a negative number will throw an exception "negatives not allowed" - and the negative that was passed. If there are multiple negatives, show all of them in the exception message

## Challenge Part 6:
- Numbers bigger than 1000 should be ignored, so adding 2 + 1001  = 2
- Delimiters can be of any length with the following format:  "//[delimiter]\n" for example: "//[***]\n1***2***3" should return 6
- Allow multiple delimiters like this:  "//[delim1][delim2]\n" for example "//[*][%]\n1*2%3" should return 6.
- make sure you can also handle multiple delimiters with length longer than one char
