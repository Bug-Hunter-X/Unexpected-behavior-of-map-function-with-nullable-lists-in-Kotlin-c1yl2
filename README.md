# Unexpected behavior of map function with nullable lists in Kotlin

This repository demonstrates an uncommon error related to the behavior of Kotlin's `map` function when applied to lists containing nullable elements.  The `map` function itself handles null and empty lists gracefully, returning an empty list in those cases.  However, if the list contains nullable elements and you aren't careful, you can encounter unexpected results or `NullPointerExceptions`.

The `bug.kt` file shows a simple example. The `bugSolution.kt` file presents solutions for handling potential null values in lists effectively.

## How to reproduce:

1. Clone this repository.
2. Open `bug.kt` and run the code. Observe the output.
3. Open `bugSolution.kt` and run the code to see the corrected output.

## Solution:

The solution involves using the safe-call operator (`?.`) and the Elvis operator (`?:`) to handle potential null values within the `map` lambda expression, ensuring that null values are handled gracefully without causing crashes.