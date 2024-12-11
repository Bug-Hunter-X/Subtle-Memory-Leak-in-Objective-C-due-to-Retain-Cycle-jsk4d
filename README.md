# Objective-C Retain Cycle Bug

This repository demonstrates a subtle memory leak in Objective-C caused by a retain cycle in manual reference counting (MRC). The bug is difficult to detect using standard debugging techniques, highlighting the challenges of manual memory management.

## Bug Description
The `bug.m` file contains code that creates a retain cycle between two objects.  One object retains the other, and vice-versa. This prevents the objects from being deallocated, leading to a memory leak.

## Solution
The `bugSolution.m` file shows how to correct the issue by ensuring proper balancing of `retain` and `release` calls, or by using Automatic Reference Counting (ARC) if possible.  In modern Objective-C development, ARC is highly recommended to avoid this type of error.