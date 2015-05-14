This is the code from the blog post "Making a simple VM interpreter in Python",
which you can find at https://csl.name/post/vm/

Made by Christian Stigen Larsen, with some improvements from the people at r/Python.
Put in the public domain.

To run:

    Hit CTRL+D or type "exit" to quit.
    > 2 3 + 5 * println
    Constant-folded (2 + 3) to 5
    Constant-folded (5 * 5) to 25
    25
    > ^D

To test:

    $ python vm.py test
    Code before optimization: [2, 3, '+', 5, '*', 'println']
    Constant-folded (2 + 3) to 5
    Constant-folded (5 * 5) to 25
    Code after optimization: [25, 'println']
    Stack after running original program:
    25
    Data stack (top first):
    Stack after running optimized program:
    25
    Data stack (top first):
    Result: OK
    ** Program 1: Runs the code for `print((2+3)*4)`
    20

    ** Program 2: Ask for numbers, computes sum and product.
    Enter a number: 12
    Enter another number: 13
    Their sum is: 25
    Their product is: 156

    ** Program 3: Shows branching and looping (use CTRL+D to exit).
    Enter a number: 1
    The number 1 is odd.
    Enter a number: 2
    The number 2 is even.
    Enter a number: 3
    The number 3 is odd.
    Enter a number: ^D
