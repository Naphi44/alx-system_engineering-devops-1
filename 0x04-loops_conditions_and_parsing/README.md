# 0x04. Loops, conditions and parsing
``DevOps`` ``Shell`` ``Bash`` ``Scripting``

# Background Context

# Resources

#### Read or watch:
- [Loops sample](https://alx-intranet.hbtn.io/rltoken/wT98UJfv_E2tk4yP9PcLLw)
- [Variable assignment and arithmetic](https://alx-intranet.hbtn.io/rltoken/olvOKX699pq50rkHRE5cSA)
- [Comparison operators](https://alx-intranet.hbtn.io/rltoken/HxohzllkOWh0t4dy_HptIQ)
- [File test operators](https://alx-intranet.hbtn.io/rltoken/g8of2ABPEJfCNtPrDQaqVw)
- [Make your scripts portable](https://alx-intranet.hbtn.io/rltoken/O0Ay21p7tDhfLMsYbtAKug)

#### man or help:
- ``env``
- ``cut``
- ``for``
- ``while``
- ``until``
- ``if``

# Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, <b>without the help of Google</b>:

# General
- How to create SSH keys
- What is the advantage of using ``#!/usr/bin/env bash`` over ``#!/bin/bash``
- How to use ``while``, ``until`` and ``for`` loops
- How to use ``if``, ``else``, ``elif`` and ``case`` condition statements
- How to use the ``cut`` command
- What are files and other comparison operators, and how to use them

# More Info
## Shellcheck
[Shellcheck](https://alx-intranet.hbtn.io/rltoken/joK6l_yEZ9N7T0GQ1RDjLA) is a tool that will help you write proper Bash scripts. It will make recommendations on your syntax and semantics and provide advice on edge cases that you might not have thought about. ``Shellcheck`` is your friend!

## Installation
Here is how to [install it](https://alx-intranet.hbtn.io/rltoken/jbz0_-i3TV3WpKgxhyrtpA).

Examples:

Not passing ``Shellcheck``:
![check fail](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/251/Vxotqyj.png)

Passing ``Shellcheck``:
![check pass](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/251/ubHWxDU.png)

For every feedback, Shellcheck will provide a code that you can use to get more information about the issue, for example for code ``SC2034``, you can browse https://github.com/koalaman/shellcheck/wiki/SC2034.
