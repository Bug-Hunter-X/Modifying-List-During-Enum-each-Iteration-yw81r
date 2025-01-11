# Elixir Bug: Modifying List During Enum.each Iteration

This repository demonstrates a common error in Elixir when attempting to modify a list while iterating over it using `Enum.each`.  The issue arises because `Enum.each` doesn't create a copy of the list; it directly operates on the original.

**The Problem:** The code in `bug.ex` attempts to remove the element `3` from the list during iteration. However, this doesn't change the list being iterated over, resulting in unexpected behavior.

**The Solution:** The correct approach, shown in `bugSolution.ex`, involves using a different approach to filter the list, like `Enum.filter` or creating a new list.