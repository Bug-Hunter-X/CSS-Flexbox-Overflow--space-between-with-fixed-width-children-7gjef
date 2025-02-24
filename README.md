# CSS Flexbox Overflow Issue

This repository demonstrates an uncommon issue that can arise when using `justify-content: space-between` in CSS Flexbox layouts.  The problem occurs when fixed-width child elements, combined with the spacing introduced by `space-between`, cause the total width to exceed the parent container's width.

The `bug.css` file contains the problematic CSS, while `bugSolution.css` offers a solution.

## Problem

The issue is that `justify-content: space-between` distributes space *between* items. If those items have a fixed width such that their total width plus inter-item space exceeds the container's width, items will overflow.

## Solution

The solution involves using `flex-shrink: 1;` on the child elements. This allows the elements to shrink if necessary to fit within the container, avoiding overflow.