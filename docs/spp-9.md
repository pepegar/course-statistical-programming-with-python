---
title: Statistical Programming with Python
author: Pepe García
email: jgarciah@faculty.ie.edu
date: 2020-04-20
lang: en
---

Statistical Programming with Python
===================================

Files


Plan for this session
=====================

-   Learn about handling files

Reading files
=============

```python
file = open("file_path")

for line in file:
    #do something with line
    pass
```

Reading files
=============

-   create a text file
-   read all its lines

Interlude: with
===============

Every time we use files we need to **close()** the file after use.  Not
closing the file would end up in an unexpected program crash.

```python
fh = open("file.txt")
# do whatever with the file here
fh.close()
```

Interlude: with
===============

In order to avoid this, Python provides the **with** keyword.  Whatever
we pass to **with** will be closed after the body.

```python
with open("file.txt") as fh:
    pass # do whatever with the file
```

Interlude: with
===============

Rewriting our previous example to use **with**

Writing files
=============

We can write to files using a similar approach

```python
with open("file.txt", "w") as f:
    f.write("this content will be written to the file!")
```

Writing files. modes
====================


When opening a file, we can choose in which **mode** we open it

Exercises
=========

```python
1. Create a function named from_csv for converting from CSV to a lists of lists.
  
2. Create a function named to_csv for converting a list of lists to CSV.
```
