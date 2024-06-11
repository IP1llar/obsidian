## Aims

The main aim of this course is to present the basic principles of programming. As the introductory course of the Computer Science Tripos, it caters for students from all backgrounds. To those who have had no programming experience, it will be comprehensible; to those experienced in languages such as C, it will attempt to correct any bad habits that they have learnt.

A further aim is to introduce the principles of data structures and algorithms. The course will emphasise the algorithmic side of programming, focusing on problem-solving rather than on hardware-level bits and bytes. Accordingly it will present basic algorithms for sorting, searching, etc., and discuss their efficiency using _O_-notation. Worked examples (such as polynomial arithmetic) will demonstrate how algorithmic ideas can be used to build efficient applications.

The course will use a functional language (OCaml). OCaml is particularly appropriate for inexperienced programmers, since a faulty program cannot crash and OCaml’s unobtrusive type system captures many program faults before execution. The course will present the elements of functional programming, such as curried and higher-order functions. But it will also introduce traditional (procedural) programming, such as assignments, arrays and references.

## Lectures

- **Introduction to Programming.** The role of abstraction and representation. Introduction to integer and floating-point arithmetic. Declaring functions. Decisions and booleans. Example: integer exponentiation.
- **Recursion and Efficiency.** Examples: Exponentiation and summing integers. Iteration _versus_ recursion. Examples of growth rates. Dominance and _O_-Notation. The costs of some representative functions. Cost estimation.
- **Lists.** Basic list operations. Append. Naïve _versus_ efficient functions for length and reverse. Strings.
- **More on lists.** The utilities take and drop. Pattern-matching: zip, unzip. A word on polymorphism. The “making change” example.
- **Sorting.** A random number generator. Insertion sort, mergesort, quicksort. Their efficiency.
- **Datatypes and trees.** Pattern-matching and case expressions. Exceptions. Binary tree traversal (conversion to lists): preorder, inorder, postorder.
- **Dictionaries and functional arrays.** Functional arrays. Dictionaries: association lists (slow) _versus_ binary search trees. Problems with unbalanced trees.
- **Functions as values.** Nameless functions. Currying. The “apply to all” functional, map. Examples: The predicate functionals filter and exists.
- **Sequences, or lazy lists.** Non-strict functions such as _IF_. Call-by-need _versus_ call-by-name. Lazy lists. Their implementation in OCaml. Applications, for example Newton-Raphson square roots.
- **Queues and search strategies.** Depth-first search and its limitations. Breadth-first search (BFS). Implementing BFS using lists. An efficient representation of queues. Importance of efficient data representation.
- **Elements of procedural programming.** Address _versus_ contents. Assignment _versus_ binding. Own variables. Arrays, mutable or not. Introduction to linked lists.

## Objectives

At the end of the course, students should

- be able to write simple OCaml programs;
- understand the fundamentals of using a data structure to represent some mathematical abstraction;
- be able to estimate the efficiency of simple algorithms, using the notions of average-case, worse-case and amortised costs;
- know the comparative advantages of insertion sort, quick sort and merge sort;
- understand binary search and binary search trees;
- know how to use currying and higher-order functions;
- understand how OCaml combines imperative and functional programming in a single language.