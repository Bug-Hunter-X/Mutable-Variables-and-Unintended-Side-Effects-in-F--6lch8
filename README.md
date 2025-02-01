# Mutable Variables and Unintended Side Effects in F# Example

This repository demonstrates a common issue in F# related to mutable variables and how they can lead to unexpected behavior when combined with functions that do not explicitly re-evaluate based on changes to these variables.

The example highlights the importance of understanding the difference between immutable and mutable data structures and the potential side effects when working with mutable data within functional programming paradigms.

## The Problem

The `bug.fs` file shows how changes made to mutable variables *after* a function call does not impact the result of that function call. This is because the function was called with specific values at the time, and any changes to those values after the fact won't retroactively change the function's output.

## The Solution

The `bugSolution.fs` file offers an approach to address the issue of unintended side effects by refactoring the code to eliminate mutable state.  This results in a more predictable and easier to reason about code base.