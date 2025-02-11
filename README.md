# Elixir List Modification Bug
This repository demonstrates a common error in Elixir when attempting to modify a list within an `Enum.each` loop.  The code intends to remove the element `3` from the list, but due to Elixir's immutability, the `List.delete` function creates a new list rather than modifying the original.

## Bug Description
The provided Elixir code iterates over a list and attempts to remove an element if it matches a specific condition. However, it fails to modify the original list as intended because `List.delete` returns a new list, not a modified original.

## Solution
The solution involves using functions that return a new modified list, such as `Enum.filter` or list comprehensions, to correctly remove the element.