# Data Drill: Working with Arrays

## Summary
In this challenge, we're going to continue exploring Ruby arrays.  We'll look at different options for creating arrays filled with data, generate some nested arrays filled with data, and then convert a nested array to a collection of hashes.  All of this is designed to get us more comfortable working with these data structures.

## Releases


### Release 0: Generate a Populated Tic-tac-toe Board
```javascript
generateTicTacToe
# => [["X", "O", "X"], ["O", "O", "X"], ["X", "X", "O"]]
generateTicTacToe
# => [["O", "O", "X"], ["X", "X", "O"], ["O", "O", "X"]]
```
*Figure 4*. Generating populated tic-tac-toe boards.

In the [data-drill-nested-arrays-challenge][] we wrote methods that returned one specific nested array. In this release, we'll again write a method that returns a nested array, but in this case, we want to add an element of randomness.

We're going to write a method `generateTicTacToe` that returns a nested array representing a [tic-tac-toe][] board.  The board should be populated with X's and O's.  We can decide how realistic to make the boards (e.g., four of one letter and five of the other, only one winner, etc.).  The only rule is that the board needs to be fully populated with X's and O's.

No tests have been provided for this method.  We'll need to write them ourselves.  Because there is an element of randomness to our method, it might seem difficult to test.  What do we know for sure about the boards we generate?

- The board has three rows.
- Each row has three columns.
- The board only contains X's and O's—nothing else.

*Note:*  Remember that RSpec has many different [matchers][built in matchers] built in.


### Release 1: Convert a Nested Array of Table Data to a Hash
```javascript
tableData = [
  ["firstName", "lastName", "city", "state"],
  ["Elisabeth", "Gardenar", "Toledo", "OH"],
  ["Jamaal", "Du", "Sylvania", "OH"],
  ["Kathlyn", "Lavoie", "Maumee", "OH"]
]

convertTable(tableData)
# => [
#  { "firstName" => "Elisabeth", "lastName" => "Gardenar", "city" => "Toledo", "state" => "OH" },
#  { "firstName" => "Jamaal", "lastName" => "Du", "city" => "Sylvania", "state" => "OH" },
#  { "firstName" => "Kathlyn", "lastName" => "Lavoie", "city" => "Maumee", "state" => "OH" }
# ]
```
*Figure 5*.  Converting table data to an array of hashes.

In this release we're going to convert a nested array into a collection of hashes.  In other words, we'll transform an array of arrays into an array of hashes.  Let's write a `convertTable` method that takes a nested array representing a data table and transforms each data row into a hash, using the table's header row data as keys (see Figure 5).

We'll need to test our method's behavior.  Given a nested array that holds table data, what does our method return?  There are a number of tests that we can write to confirm that our method is behaving as we expect.  Our code is not complete without tests.


### Release 2:  Stretch *(optional)*
*This release is optional.*

In *Release 2* we converted some table data represented as a nested array into an array of hashes.  How did we pair the table headers with each row's data?  How did we create the hashes?  Ruby provides a number of handy methods for working with and creating arrays and hashes.  For example, there's the `Hash::[]` class method which converts a properly formatted array into a hash.  Take some time to read through the [documentation][Hash Documentation] on this method.  Note that the array we pass to the method can actually be formatted in different ways. Which format seems most convenient, given the table-like structure that we're working with?  As always, we can test out the `Hash::[]` method in IRB to see how it behaves.

Refactor our code to take advantage of this and other methods that Ruby provides us.  


## Conclusion
This challenge has given us practice working with arrays and hashes.  These are two fundamental data structures with which we need to be familiar.  We need to know how to instantiate them, manipulate them, transform them, access their values, etc.  Before moving on, let's be sure that we've answered any questions that popped up in this challenge.


[built in matchers]: https://www.relishapp.com/rspec/rspec-expectations/v/2-14/docs/built-in-matchers
[data-drill-nested-arrays-challenge]: ../../../data-drill-nested-arrays-challenge
[Hash Documentation]: http://ruby-doc.org/core-2.2.0/Hash.html#method-c-5B-5D
[tic-tac-toe]: https://en.wikipedia.org/wiki/Tic-tac-toe
