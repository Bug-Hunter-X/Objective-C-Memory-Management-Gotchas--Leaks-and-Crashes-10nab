# Objective-C Memory Management Issues

This repository demonstrates a common, yet often subtle, set of bugs related to memory management in Objective-C.  Specifically, it highlights issues that can occur when dealing with object ownership and the use of blocks.

## The Problem

In Objective-C, proper memory management is crucial.  Incorrectly handling the retain/release cycle (or, even with ARC, improper understanding of object lifecycles) can lead to memory leaks and crashes. The example code shows how easily these issues can arise, even with seemingly straightforward code.

## How to Reproduce

1. Clone this repository.
2. Open the `bug.m` file to see the problematic code.
3. Compile and run.  Observe the memory leaks or crashes (depending on the specific issue demonstrated).

## The Solution

The `bugSolution.m` file provides corrected code that addresses the identified memory management problems.

## Key Learnings

*   Always be mindful of object ownership and the retain/release cycle (or strong/weak references in ARC).
*   Use appropriate techniques to avoid memory leaks, particularly when dealing with long-lived objects or objects held in collections.
*   Understand the implications of capturing `self` within blocks, especially in situations where the block might outlive the object.