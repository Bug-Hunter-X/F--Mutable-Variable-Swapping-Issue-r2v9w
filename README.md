# F# Mutable Variable Swapping Issue

This example demonstrates a common issue when working with mutable variables in F#. The `swap` function attempts to swap the values of `x` and `y`, but due to the way mutable variables are passed, it does not produce the expected result.

## Problem Description

The `swap` function does not correctly swap the values of x and y when using mutable variables.  The values of x and y passed into swap are copies of the values of x and y from the outer scope. The swap function only modifies these copies.  This means the original mutable variables x and y in the outer scope are not changed. 

## Solution

The solution involves using the `ref` cell type to pass the mutable variables by reference, allowing the `swap` function to modify their values directly.