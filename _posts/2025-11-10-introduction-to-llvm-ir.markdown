---
layout: post
title: "LLVM IR 101: Understanding the Intermediate Representation"
date: 2025-11-10 10:00:00 +0530
categories: [compilers, llvm]
tags: [llvm, ir, compilers, optimization]
author: Nouman Amir
excerpt_separator: <!--more-->
---

LLVM's Intermediate Representation (IR) is the core of its entire ecosystem. It's a low-level, assembly-like language that is designed to be well-defined, lightweight, and hardware-independent. Understanding the IR is the first step to becoming proficient in compiler development with LLVM.

<!--more-->

### The Three Forms of LLVM IR

LLVM IR exists in three equivalent forms:

1.  **In-memory:** The actual data structure used by the compiler passes for transformations.
2.  **Bitcode:** The compact, binary file format (usually ending in `.bc`).
3.  **Human-readable assembly:** The readable text format (usually ending in `.ll`).

We primarily work with the human-readable format for debugging and analysis.

### A Simple Example: Adding Two Integers

Consider this simple C function:

```c
int add(int a, int b) {
    return a + b;
}
