---
layout: project
title: Minesweeper
subtitle: An AI that plays minesweeper
---

Computer plays minesweeper!

#### About Minesweeper:

Minesweeper is a puzzle game that consists of a grid of cells, where some of the cells contain hidden “mines.” Clicking on a cell that contains a mine detonates the mine, and causes the user to lose the game. Clicking on a “safe” cell (i.e., a cell that does not contain a mine) reveals a number that indicates how many neighboring cells – where a neighbor is a cell that is one square to the left, right, up, down, or diagonal from the given cell – contain a mine.

#### The project

This is a pygame project, where a minesweeper game board is represented by an 8x8 game board, and each cell is represented as a tuple (i, j). 

The overall game has been represented using first-order logic, where each sentence is of the form:
```
{A, B, C, D, E, F, G, H} = 1
```
This representation has two parts: a set of cells on the board that are involved in the sentence, and a number `count`, representing the count of how many of those cells are mines. The above logical sentence says that out of cells A, B, C, D, E, F, G, and H, exactly 1 of them is a mine.

Using this representation, we can form statements of the form `{X, Y, Z} = 0` to mean that out of cells X, Y, and Z, exactly 0 of them are mines. And, all the cells in the set `{X, Y, Z}` are safe. Similarly, `{A, B, C} = 3` means that all of A, B, C are mines.

Also, consider two sentences `{A, B, C} = 1` and `{A, B, C, D, E} = 2`.  We could then infer a new piece of knowledge, that `{D, E} = 1`. After all, if two of A, B, C, D, and E are mines, and only one of A, B, and C are mines, then it stands to reason that exactly one of D and E must be the other mine.

More generally, any time we have two sentences `set1 = count1` and `set2 = count2` where `set1` is a subset of `set2`, then we can construct the new sentence `set2 - set1 = count2 - count1`

#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/minesweeper)

