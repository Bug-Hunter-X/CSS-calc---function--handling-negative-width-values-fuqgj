# CSS calc() Function: Handling Negative Width Values

This repository demonstrates an uncommon error related to the CSS `calc()` function and its interaction with percentages.  The error occurs when the calculation results in a negative width, which some browsers don't handle consistently.

The `bug.css` file contains the erroneous code that causes this issue. The `bugSolution.css` offers a fix to provide robust behavior.

## Problem

The `calc(50% - 10px)` expression works fine when the parent container is sufficiently wide. But when the parent's width is small enough to make `50% - 10px` negative, unexpected layout results might occur.  The browser might treat the negative width as 0, or there might be rendering inconsistencies across browsers.

## Solution

The solution involves adding a `max-width` or a conditional statement to ensure that the width never becomes negative.  This creates a more robust and cross-browser compatible solution.