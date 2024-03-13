---
type: assignment
date: 2024-03-11T11:59:00+5:00
title: "Assignment #2: Pairwise Global Alignment"
published: true
#pdf: /static_files/assignments/asg.pdf
#attachment: /static_files/assignments/asg.zip
#solutions: /static_files/assignments/asg_solutions.pdf
#published: true
due_event: 
    type: due
    date: 2024-04-03T11:59:00+5:00
    description: 'Assignment #2 due'
---


# Assignment 3 (global pairwise alignment) : Overview

This assignment deals with pairwise alignment of strings.  We covered many
different variants of the alignment problem in class.  For this project, we
will be concerned with the global alignment of strings under the global, linear
gap, scoring function (the variant we covered in class). Throughout this
document (and in the project), we will follow the convention that the string X
is considered the _query_ while Y is considered the _reference_.

Unlike projects 1 and 2, you will implement only 1 program for this assignemnt.

You will implement global alignment, with _linear_ gap costs (the simplest) between pairs of strings.  You will compute both the score of the optimal alignment between the strings as well as the edits that yield this optimal score. 
You will write down the optimal alignment in terms of the backtrace through the alignment matirx, explained below.

**NOTE** : The timeout for all tests for the gradescope server will be 30 minutes

## Overall structure

You will submit your assignment as a tarball named `BIOI607_A3.tar.gz`.  When this tarball is expanded, it should create a **single** folder named `BIOI607_A3`.  This folder must be created in the directory where the decompression (i.e. `tar xzvf`) is done, and must not be nested inside any other folders. The details of how you structure your "source tree" are up to you, but the following **must** hold (to enable proper automated testing of your programs).

 * There should be a script at the top-level of `BIOI607_A3` called `build.sh`.  This should do whatever is necessary to create 1 executable at the top level called `saligner`.  If you're comfortable with Makefiles, this can just call `make`, or it could simply run the commands necessary to compile your programs and copy them to the top-level directory.  You can assume this script is run in a `bash` shell.
 
 * There should be a `README.md` file in the top level directory.  This README file should contain the following information.
     
     - What language have you written your solution in?
     - What did you find to be the hardest part of this assignment?
     - What resources did you consult in working on this assignment (view this as a form of citation; you shouldn't _copy_ code directly from anywhere in your assignment, but if you consulted other sources please list them here).

**Turnin** : The assignment turnin will be handled using Gradescope. The Gradescope submission and autograder for this project should be visible on the course Gradescope website. 

## Input 

Since there is only one program being written in this project, the input will be unfiorm over all invocations of the program.  Therefore, we describe the input here.  Your program `saligner` should take 5 arguments, given in this order:

* `input_file` - the path to an input file of string pairs in the format specified below.
* `mismatch_penalty` - this is a positive integer `m`, such that the score of a mismatch in an alignment will be `-m`.
* `gap_penalty` - this is a positive integer `g`, such that the score of each gap character inserted into the alignment will be `-g`.
* `output_file` - the path to the file where your output will be written.

### Input pair format

The `input_file` provided to your program will have a collection of `ProblemRecord`s, and your program should align the pair of strings in each `ProblemRecord` and produce output in the specified format below. Each `ProblemRecord` consists of _exactly_ 3 lines in the input file and is of the format:

```
problem_name
X
Y
```

where `problem_name` is simply an arbitrary (unique) string that identifies this alignment problem and `X` and `Y` are strings over the DNA alphabet (`A`,`C`,`G`,`T`).  For example, here is a `ProblemRecord`:

```
p-0
GGTGGAGATACGGGCTCCAA
CGTGGAGGTACGGGCA
```

The `problem_name` is `p-0`, `X` is `GGTGGAGATACGGGCTCCAA` and `Y` is `CGTGGAGGTACGGGCA`.

The input file will simply consist of a collection of such records, written back to back in the file.  So, for example, if there are 100 `ProblemRecord`s in the input file, there will be 300 lines.

### Output format

The output written by your program will consist of a set of `OutputRecord`s.  The `OutputRecord`s **must appear in the output file in the same order as the `ProblemRecord`s in the input file**.  Each `ProblemRecord` in the input will yield exactly one `OutputRecord` in the output. Each `OutputRecord` is exactly 3 lines long, and it has the following format:


```
p-0 score aln_len
aligned_X
aligned_Y
```

The first line of the `OutputRecord` records relevant information about the problem instance; the problem name, the optimal score achieved, and the lenth of the strings under the 
global alignment that follows.

* `problem_name` - this is the original name of the problem instance in the input
* `score` - this is the optimal score as computed by your dynamic program
* `aln_len` - this is the length of the traceback through the dynamic programming matrix, or, in other words, the length of X and Y, including any gap characters, under the optimal alignment 

After this first line, eahc `OutputRecord` contains 2 more lines, which are the context of the `X` and `Y` strings under the optimal alignment (i.e. as printed from the traceback including 
any gaps within them).  The second line of the `OutputRecord` contains the aligned `X` string and the third line contains the aligned `y` string.

_Crucially_, your **alignment strings must** be (1) consistent with your reported score (i.e. `-m` x mismatches + (`-g` x (insertions + deletions)) = score) and (2) walking the strings X and Y and applying the observed mismatches and gaps must transform `X` into `Y`. An example of an `OutputRecord` for the input record `p-0` above is :

```
p-0 -14.0 20
GGTGGAGATACGGGCTCCAA
CGTGGAGGTACGGGC---A-
```

This was computed with `m` = 1 and `g` = 3, so the score of a mismatch is -1, the score of a gap is -3, and the score of a match is 0.  This output tells us that the best scoring alignment between `X` and `Y` is -14. Because this is a global alignment, the alignment starts at position 0 of Y and ends at position 16 of Y (Y's length).  The alignment is 20 characters long. Finally, the next 2 lines contain the strings `X` and `Y` with the appropriate gap characters added.

### Grading

**Critically**, to obtain credit for a proper alignment you _must_ be able to write out the appropriate traceback — not just compute the score of the best alignment. **However**, the alignment problems will be evaluated independently, so you can obtain partial credit for having correct alignments for some of the problems even if you don't have correct alignments for all of them. Finally, as we discussed in class, there can be many optimal alignments of the same score. While you must produce _an_ optimal alignment to obtain credit for a problem instance, you need not report a particular optimal alignment.  Rather, it must be optimal (of the highest score) and consistent (the alignment printed in the `OutputRecord` must actuall achieve this score and transform `X` into `Y`).
