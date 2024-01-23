---
layout: page
title: Course Materials
permalink: /materials/
---

<!--{% include image.html url="/_images/cover2.jpg" width=175 align="right" %}-->

# Syllabus for BIOI607: Algorithms and Data Structures for Bioinformatics

Here you'll find an overview of the course — the material I expect we'll cover, the breakdown of course assignments and credit, and the course policies.

## Assumed prerequisites

While there are no enforced course prerequisites for this class, we will assume a basic mathematical maturity and familiarity with 
certain mathematical ideas.  Because no specific computer science prerequisites are assumed, we will have to spend some time covering the 
basics of what will be required to understand the data structures and algorithms we will cover in class.  This includes:

  * Basic data structures and algorithms (arrays, lists, trees, hashing, divide-and-conquer, dynamic programming, greedy algorithm design, etc.)
  * Basic CS theory and asymptotic notation (the word-RAM model, familiarity wih big O notation, and perhaps little o, and Theta notation)
  * Basic programming skills.  I will try to cover this in a language agnostic way, but examples will ususally be given in a specific language.

## Logistics

* Course Website : [https://umd-bioi607.github.io/s2024](https://umd-bioi607.github.io/s2024)
* Instructor : Rob Patro
* Instructor office hours: by appointment
* Class location: IRB 2207
* Class days/time:  Wed. 6:00 PM — 8:45 PM

<!-- * **Lecture recordings** : I plan to make a best-effort attempt to record the lectures in this class. However, **watching a pre-recorded lecture is not, in general, a sufficient proxy for attending the lecture in person (there are numerous reasons for this that I'd be happy to discuss in person)**. Therefore, the policy in this class for recordings is the following: I will attempt (subject to overcoming technical difficulties) to record the lectures, but I will not, by default, post them on Panopto. If you need to miss class for a health-related reason (or any legitimate reason), just send me an e-mail and I will be happy to provide a recording of the lecture you missed. I hope this policy provides the benefits of recorded lectures while mitigating some of the detriments. -->

## Course Content

**Links**: 

 * In general, _this website_ is the place to look for course content and course news.  Any content that is private / restricted (e.g. grades) will be made available on the ELMS page for this course.
<!-- * Assignment announcements and deadlines will be posted on the [ELMS page for this course](https://umd.instructure.com/courses/1338959), and grading information will be made available there. -->
 * The course also has a Piazza page for discussions.  Please register for this course on Piazza [here](https://piazza.com/umd/spring2024/bioi607).

**Textbook(s)**: There is no required text for this course, however if you are interested in independent reading and are looking for a specific book that is reasonably aligned with this course, I would suggest you check out [Bioinformatics: An Active Learning Approach](https://www.bioinformaticsalgorithms.org).

**Basics of algorithms and data structures**:

Though we will cover the basic algorithms and data structures we need in this course, you may find that you need to spend more time learning about these concepts.  Additionally, you may want to dive deeper into these *interesting* topics. I recommend the following resources:

- [Algorithms](http://algorithmics.lsi.upc.edu/docs/Dasgupta-Papadimitriou-Vazirani.pdf) (Dasgupta, Papadimitriou, and Vazirani 2006)
- [Algorithm Design](http://www.amazon.com/Algorithm-Design-Jon-Kleinberg/dp/0321295358) (Kleinberg and Tardos 2006)
- [Introduction to Algorithms, 3rd edition](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844)(Cormen, Leiserson, Rivest and Stein, 2009)

**Genomics algorithms, data structures, and statisitcal models**:

I recommend the following supplementary material with respect to genomics algorithms in particular:

- [Genome Scale Algorithm Design](http://www.cs.helsinki.fi/group/gsa/book/) (Mäkinen, Belazzougui, Cunial, Tomescu 2015)
- [Biological Sequence Analysis](http://www.amazon.com/Biological-Sequence-Analysis-Probabilistic-Proteins/dp/0521629713) (Durbin, Eddy, Krogh, Mitchinson 1998)

**Molecular biology**:

We will cover the basic required molecular Biology in the course. However if you're not familiar with basic molecular Biology, there are some useful resources worth reading:

- [Molecular Biology of the Cell](http://www.ncbi.nlm.nih.gov/books/bv.fcgi?call=bv.View..ShowTOC&rid=mboc4.TOC&depth=2) (Alberts,  Johnson,  Lewis,  Raff,  Roberts and  Walter, 2002)
- [Molecular Biology: Principles of Genome Function 2nd Edition](https://www.amazon.com/Molecular-Biology-Principles-Genome-Function/dp/0198705972/) (Craig,  Green, Greider, Storz, Wolberger, Cohen-Fix, 2014)
- [Molecular Biology](http://www.amazon.com/Molecular-Biology-Second-Edition-David/dp/0123785944) (Clark and Pazdernik 2012)


**Programming, software development, and using the command line**

In general in this course, we are going to be doing some programming.  There are many ways to develop software, but the vast majority of bioinformatics software runs from, and is developed with, command line tools.  Therefore, we will learn the basics of using these tools (e.g. how to properly create a tarball, how to invoke the compiler from the command line / a script, etc.).

I realize it may have been a while since you have used these skills, or you may not have learned them at all. If you feel you need a refresher on these topics, or as an alternative resource to what I will cover, I would strongly suggest checking out [“The missing semester”](https://missing.csail.mit.edu/) (an MIT course dedicated to these various miscellaneous topics).


**Expectations**: Since this is a course on data structures and algorithms for bioinformatics, you will be expected to become familiar with the relevant biology — it is an important and inextricable part of the material, and the underlying biology provides motivation for the computational problems we will tackle. However, our focus will be on the computational aspects of bioinformatics and genomics. 

## Course Objectives

The main objective of this course will be to provide an understanding of some of the algorithms, data structures, and methods that underlie _modern_ computational genomics. This course is intended as a broad introduction to common data structure and algorithms in genomics, and the problems that some of these algorithms are intended to solve.  However, this is a huge field, so we will certainly not cover everything, and what we do cover will not all be at the same depth. Our perspective will be a computational and algorithmic one, though we will take the time to understand the necessary biology and motivation for the problems we discuss. At the end of this course, you should have a good understanding of how new challenges in genomics drive algorithmic innovations and how algorithmic innovations enable new and improved biological analyses.

## Course  Schedule

The following is a planned schedule of the material we will cover in the course, as well as when we will cover it. The mapping between content and dates below _is subject to change_ depending on how quickly we move, and even some of the topics themselves are subject to change if we get deep into a topic and the class expresses interest in going further. The current schedule is likely optimistic, and I would like to cover all of this material. However, it's much more important that the class understand the material we cover than that we get to all of the topics I'd like to discuss. Thus, the time we spend on certain topics and the precise list of topics we cover is subject to change throughout the semester depending on our pace.

### Tentative coverage of topics

- Week of Jan 22.
  - Course introduction, logistics & goals
  - Basic biology fundamentals, genomics concepts and motivating problems

- Week of Jan 29.
  - Fundamental challenges in genomics : Indexing and Search Overview
  - Necessary CS concepts: Arrays, sorting, binary search
  - "Classic" indexing structures : suffix array
    - Practical uses of the suffix array (MUMMER, STAR aligner)

- Week of Feb 5.
  - Advanced suffix array concepts
  - Maximum Mappable Prefix, Prefix lookup
  - Necessary CS Concepts: Hashing, Hash Tables 

- Week of Feb 12. 
  - Word-based indexing, k-mers, minimizers, strobemers
  - Inverted indices in general, benefits and tradeoffs from the suffix array

- Week of Feb 19.
  - Return of the full-text index: the BWT and FM-index

- Week of Feb 27.
  - Rank, select, and basic succinct data structures
  - Minimal perfect hashing (BBhash data structure; maybe PTHash)
  - Project selection & groups due

- Week of March 5.
  - "Signature" schemes : minimizers, syncmers, strobemers, k min-mers
  - The de Bruijn graph and compacted de Bruijn graph

- Week of March 12.
  - Constructing the compacted (colored) de Bruijn graph efficiently 
  
- Week of March 17.
  - **No class: Spring Break**

- Week of March 25.
  - More on constructed the compacted (colored) de Bruijn graph efficiently
  - Reference indexing using the compacted de Bruijn graph 

- Week of April 1.
  - Unitigs, simplitigs and spectrum preserving string sets
  - Large-scale sequence search; Sequence Bloom Tree and variants
  - Final project progress report due

- Week of April 8.
  - Large-scale sequence search (continued)
  - Mantis, color set compression and the counting dBG
  
- Week of April 15.
  - Single-cell transcriptome profiling, barcoding, UMI-resolution
  - Rob away April 18

- Week of April 22.
  - Downstream (computational) challenges in single-cell analysis
  - Representation, visualization, feature selection, sketching, clustering, integration
  
- Week of April 29.
  - Final project presentations

- Week of May 6.
  - Course wrapup
  - May 9th is last day of class

- Fri May 10.
  - Final exam available

- Mon May 13.
  - Final exam due by 11:59PM

- Thurs May 16.
  - Final project reports due by 11:59PM

## Course Resources

The course website is [https://umd-cmsc701.github.io/s2024](https://umd-cmsc701.github.io/s2024), which is probably where you are reading this right now.

The course has a Piazza page, and you can enroll [here](http:///www.piazza.com/umd/spring2024/cmsc701).  I encourage you to interact with each other, raise questions, and discuss course topics using Piazza.  This is also the best place to raise general questions about material we cover in the course (as opposed to e.g. an e-mail), since other students can see the response and ask follow-up questions.  This helps to reduce redundancy in the answering of questions.

## Course Policies

**Coursework and grading**: The coursework will consist of 2-3 homework projects, a final project, and a final exam. Students will have an opportunity to select their final project in Feb.; there will be a few projects to choose from, and students will also be allowed to propose their own projects. The projects are to be done, ideally, in teams of 3 (I will allow the project to be done solo with approval, an _may_ approve a team of 4 if there is a compelling reason). Further, the grade for the final project will be broken down into components for the interim report, a final project presentation, and the final project delivery itself. For the final project, the final deliverables will consist of runnable code (including a link to a version-controlled repository containing the source), and a short (4-5 page) research-style paper describing the work you’ve done. The breakdown of weights for these different assignments will be as follows:

- Homeworks - 25%
- Final Project - 50%
  - Interim report 10%
  - Final presentation 10%
  - Final report 30%
- Final Exam — 25%

**Programming languages for homeworks**: As we will see throughout the course, modern computational genomics places a great emphasis on efficiency.  A very large part of this, of course, is algorithms and data structures, but another important part is the details of how these are implemented and the efficiency of the underlying implementation.  As a result, it's a requirement that the programming assignments (but not necessarily the final project) be completed in a _compiled_ (and ideally native) programming language.  Examples of languages that meet this requirement include Rust, Go, Nim, Zig, C, C++, Java, Kotlin and Scala. There are, of course, many others, and if you have a desire to use a specific language outside of this list, please just check with me first. However, languages like Python and R are not appropriate for the programming assignments we will be doing in the course and shouldn't be used.

**Late policy**: Assignments that are turned in late will be docked 1% for each hour they are late up to the first 48 hours.  After 48 hours, late assignments will not be accepted.  Each student is allowed *one* free late assignment turnin (you can turn the assignment in up to 48 hours late with no penalty).  However, you must let me know that you are using your free late assignment _when you turn in your assignment_, and the decision is non-revocable (if you decide to use the free late assignment for assignment 1, you can't than request to take the late penalty for 1 and use the late assignment for assignment 2).

**Regrade policy**: All requests to re-grade, re-check, or re-mark an assignment or exam question **must be made in writing**. When the assignment is re-graded, it will be re-checked in its entirety. This means that *it is possible to lose points on other problems if they were graded incorrectly or too leniently the first time*. Therefore, I urge you to thoroughly consider each regrade request you make.

### Absences / scheduling accomodations 

  - medical reasons: (Obviously,) If you are exhibiting any symptoms indicative of COVID-19, **please do not attend class in person**.  Instead get tested (either at the [University health center](https://uhr.umd.edu/coronavirus/return-to-campus/covid-19-testing-information/) or elsewhere).  Likewise if you believe that you may have been exposed (i.e. have been in close contact for an extended period of time with someone with a confirmed infection), please do not attend class and instead get tested. If, for a health-related or medical reason, you will miss two or more consecutive classes, or will miss class on a recurring basis, or were unable to meet a particular academic obligation of this course, I will require a written note from the Student Health Service or a healthcare provider documenting the range of dates for which you were unable to meet your academic obligations. This note need not contain any diagnostic information. 
  
  - non-medical reasons: If you will miss any classes or scheduled exams as a result of religious observances, you must submit this information to me, in writing, within the first two weeks of the semester to make necessary accommodations to complete the work that will be missed. In this course, this applies mostly to notifying me about expected absences from class.  The homeworks and projects are assigned far-enough in advance that it is not reasonable that extensions or delays be provided for religious reasons.

**Final Grades**: The grade you receive in this class will reflect, as much as possible, the degree to which you have mastered the necessary material. How much somebody “needs” an ‘A’ will have no bearing on whether or not (s)he receives an ‘A’, other than how this need or desire is reflected in the work that (s)he does. I want everyone to do well in this course, and will make every reasonable effort to help you understand the material as well as possible. However, barring errors in the grading of assignments, the grades you receive at the end of the semester are final, and I will not alter them for personal or non-academic reasons, *so please do not ask me to*!

### Academic integrity

*TLDR* : Don't cheat.  Don't copy code from friends, classmates, or the internet for the programming assignments. Don't provide code to classmates for any of the assignments or projects.  Don't cheat on the exams.  Be cool, and everything will be cool.

*Long form* : [From the University's Undergraduate Catalog Statement on Academic Integrity ](https://academiccatalog.umd.edu/undergraduate/registration-academic-requirements-regulations/academic-integrity-student-conduct-codes/):

> The University of Maryland is an academic community. Its fundamental purpose is the pursuit of knowledge. Like all other communities, the University can function properly only if its members adhere to clearly established goals and values. Essential to the fundamental purpose of the University is the commitment to the principles of truth and academic honesty. Accordingly, the Code of Academic Integrity is designed to ensure that the principle of academic honesty is upheld. While all members of the University share this responsibility, the Code of Academic Integrity is designed so that special responsibility for upholding the principle of academic honesty lies with the students.

> The University's Code of Academic Integrity is a nationally recognized honor code, administered by a Student Honor Council. Any of the following acts, when committed by a student, shall constitute academic dishonesty:

 * Cheating: fraud, deceit, or dishonesty in any academic course or exercise in an attempt to gain an unfair advantage and/or intentionally using or attempting to use unauthorized materials, information, or study aids in any academic course or exercise.
 
 * Fabrication: intentional and unauthorized falsification or invention of any information or citation in any academic course or exercise.

 * Facilitating academic dishonesty: Intentionally or knowingly helping or attempting to help another to violate any provision of the Code of Academic Integrity.
 
 * Plagiarism: Intentionally or knowingly representing the words or ideas of another as one's own in any academic course or exercise.
 
> If it is determined that an act of academic dishonesty has occurred, a grade of "XF" is considered the normal sanction for undergraduate students. The grade of "XF" is noted on the academic transcript as failure due to academic dishonesty. Lesser or more severe sanctions may be imposed when there are circumstances to warrant such consideration. Suspension or expulsion from the University may be imposed even for a first offense.

Academic integrity is a very serious issue. Any assignment, project or exam you complete in this course is expected to be your own work. If you are allowed to discuss the details of or work together on an assignment, this will be made explicit. Otherwise, you are expected to complete the work yourself. *Plagarism is not just the outright copying of content*. If you paraphrase someone else's thoughts, words, or ideas and you don't cite your source, this constitues plagraism. It is always much better to turn in an incorrect or incomplete assignment representing your own efforts than to attempt to pass off the work of another as your own. **If you are academically dishonest in this course, you will recieve a grade of XF, and you will be reported to the university's Office of Student Conduct**.

### Accessibility and Disability Service, ADS

Any student eligible for and requesting reasonable academic accommodations due to a disability is requested to provide, to the instructor in office hours, a letter of accommodation from the Office of Accessibility and Disability Services (ADS) within the first two weeks of the semester. If for some reason ADS accommodation is only granted to a student mid-semester, it applies to coursework from then on, not retroactively. **Please note:** Students must make accommodated testing reservations 3 business days in advance of the test date.


### Inclement Weather Policy

You can find information about the University's inclement weather and weather-related delay and closure policies [here](https://umd.edu/weather).

In the event that campus is closed due to inclement weather, I will announce *as soon as possible* (but no sooner) whether our lecture is canceled, or whether it will be delivered remotely (via Zoom). In the latter case, I will make a post to Piazza with the Zoom link to be used for the lecture.

