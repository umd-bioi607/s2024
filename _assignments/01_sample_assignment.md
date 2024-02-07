---
type: assignment
date: 2024-01-31T4:00:00+4:30
title: 'Assignment #0 - Using the command line and parsing input'
#pdf: /static_files/assignments/asg.pdf
#attachment: /static_files/assignments/asg.zip
#solutions: /static_files/assignments/asg_solutions.pdf
published: true
due_event: 
    type: due
    date: 2024-02-09T4:00:00+4:30
    description: 'Assignment #0 due'
---

**Posted: Wed Jan 31, 2024**  
**Due: Thurs Feb 9, 2024**  

As you develop your proejct, I **highly, highly** recommend that you use [`git`](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) for developing your code. The easiest way to do this is to use [`GitHub`](https://www.github.com).

# Overview

This assignemnt has one component:

A program that parses valid (possibly multi-line) FASTA files, computes certain simple statistics, and writes them to a JSON format output.

## Overall structure

You will submit your assignment as a `tarball` named `BIOI607_A0.tar.gz`.  When this tarball is expanded, it should create a folder named `BIOI607_A0`.  The details of how you structure your "source tree" are up to you, but recommendations are below.

  
 * There should be a `README.md` file in the top level directory.  This README file should contain the following information.
     
     - What resources did you consult in working on this assignment (view this as a form of citation; you shouldn't _copy_ code directly from anywhere in your assignment, but if you consulted other sources please list them here).

### How to create the proper structure for your project

First, we'll create a directory to hold our source and change into it:

```
> mkdir BIOI607_A0
> cd BIOI607_A0
```


Then, we need to create our source file.  For now, we'll just create a dummy file:

```
> echo "Hi, Rob" > README.md
> echo "!#/usr/local/env python3" > fasta_stats
```

Finally, to create the "tarball" from our directory, we do the following.  First, we back up one level in the directory hierarchy:

```
> cd ..
```

Then, we run the following command:

```
> tar czvf BIOI607_A0.tar.gz BIOI607_A0
```

This should create an output file called `BIOI607_A0.tar.gz` in the current directory, which is something you can upload.

**Turnin** : The assignment turnin will be handled using Gradescope.  

## The FASTA stats program

You will write a program that reads and parses a `FASTA` format file and generates statistics about the records in the file. Your program will take a single command line parameter (the path to the input file).  The output will be written to `stdout`. This also means that you should not write any other messages to `stdout` — if you need to write diagnostic messgages from your program, you should write them to `stderr`. Your program should be called `fasta_stats`.

**Note**: In `python`, the standard `print()` function writes to `stdout` by default, so that's where everything will be going if you are writing it with `print()`.

### Input 

The input consists of 1 argument:

* `input_file` - the path to a `FASTA` format file containing the genome records that you should parse.

Each records in the `FASTA` format consists of 2 parts, a _header_ line (which starts with the `>` character, followed by a record identifier). The first string after `>` in each record header will provide a _unique_ identifier for this record. After this record identifier, there may be zero or more other strings providing extra information. You need not worry about them for the purpose of this project. After the header comes the _sequence_ of the record. The sequence consists of a sequence of one or more lines. Each line consists of a sequence of characters (in this case they will all be `A`, `C`, `G` or `T`). The _sequence_ for a record may span more than one line, in which case the total sequence associated with this record is **the concatenation of all sequence lines, removing any occurrences of the `\n` character**.  There is no _a priori_ limit on the length of lines, or the length of the sequence string they encode.  This means that your parser should implement the appropriate logic when reading a record (i.e. scanning and concatenating the sequence for a record until it encounters the end of the file or the next header).  The `FASTA` file itself, then, just consists of a sequence of such records.

### Output 

#### Statistics

Your program should write to `stdout` a JSON format object (string) with the following information (using the following keys, each associated with the proper value):

* `min_len` - The length of the shortest _sequence_ observed for any record (this is the total sequence length, which may comprise multiple input lines if this is a multi-line record).
* `max_len` - The length of the longest _sequence_ observed for any record (this is the total sequence length, which may comprise multiple input lines if this is a multi-line record).
* `mean_len` - The average length of sequences observed for the records in the input file.
* `tot_len` - The total length of sequences observed for the records in the input file.
* `num_records` - The total number of input records observed in the input file.
* `count_a` - The total number of occurrences of the nucleotide `A` appearing in this file.
* `count_c` - The total number of occurrences of the nucleotide `C` appearing in this file.
* `count_g` - The total number of occurrences of the nucleotide `G` appearing in this file.
* `count_t` - The total number of occurrences of the nucleotide `T` appearing in this file.

This information should be written as a properly-formatted `JSON` object to `stdout`.
