java c
CS917 Foundations of Computing 
– Algorithms Coursework 
2024/2025
Submission Details This assessed piece of coursework must be submitted by Noon  12:00,  Monday,  25th November 2024. Submission is done electronically via Tabula, and two files are expected for submission:
1. A PDF of your solutions named Answers.pdf.
2. A file named SuffixTreeSearch.py of your python solution for the parts of Question 7.
The solutions submitted must be your own work.  You are expected to work indepen- dently, not in groups.
Marking 
1.  Please show the full work progress where appropriate, detailing how you have arrived at your answer.
2. We don’t subtract marks, but you earn marks.   Marking criteria are correctness of results; quality of analysis and reasoning, which involves backing up your arguments with relevant examples; the relevance, quality and conciseness of your argumentation; organisation and presentation of results  (correctly labelled graphs,  etc.);  quality of code (well structured, annotated and documented, computationally efficient).
3.  To achieve very high marks (> 80%), you are expected to clearly exceed expectations of what is considered a correct solution together with an explanation.  This could for example involve providing a highly efficient solution together with a proof of complex- ity, demonstrating that you engaged with the scientific literature, or demonstrating exceptional understanding of a problem through a concise discussion or interpretation.
4.  Follow the guidelines on using generative AI tools found in the Handbook (https:// warwick.ac.uk/fac/sci/dcs/teaching/handbook/coursework), specifically on how to quote them and keeping a log of your chat protocol.
Questions 
Question 1 (10 points) For each function f(n) and time t in the following table, determine the largest size n (an integer) of a problem that can be solved in time t, assuming that the algorithm to solve the problem takes f(n) microseconds. Where possible, formulate the analytical solution to the problem by solving for n and compute the answer with the help of an electronic calculator (or Python).  If you need to solve a problem numerically, you can use Python to assist in working out answers. Explain your work progress, not just write down the answers. (We will assess your work progress based on whether you have shown a clear understanding of the problem and that you have solved this problem independently; simply writing down the answers without explanation will receive no marks).

1 second 
1 minute 
1 hour 
1 day 
nlog2 n 




√2n2 




n3 




√n 




n! 




Question 2 (10 points) 
Where possible, apply the master theorem for the following.  If not possible, state the reason why.
(a) T(n) = 7T(n2) + 47n
(b) T(n) = 2nT(n2) + n
(c) T(n) = 16T(n4) + 16n2
(d) T(n) = 4T(53n) + 50n3
(e) T(n) = 8T(n/4) + f(n) and all you know about f(n) is that f(n) = Ω(n)
Question 3 (10 points) For each of the following input lists, state what you believe to be the most effective sorting algorithm. Use only the algorithms that are covered in the lecture.  Justify your reasoning, taking into account complexity, number of operations, memory usage and any other properties of sorted lists. If there are features or attributes of the algorithm that are implementation dependent, state these in your answer.
(a)  [1, 2, 4, 3, 5, 6, 7, 10]
(b)  [13, 12, 9, 6, 5, 4, 3, 2, 1]
(c)  [1, 10, 5, 8, 3, 9, 6, 4, 2]
(d)  [6,  5, 6, 5, 9,  11, 1, 23, 7].  Two objects with the same values need to preserve their order after sorting.(e)  [(3, 9),  (4, 5), (4, 4), (9, 5), (8, 7), (10, 6)] where each tuple (key, value) is sorted by the key. The ordering of the values must be preserved where the keys are equivalent.
Question 4 (5 points) 
Apply Dijkstra’s Algorithm to the following graph,  computing the shortest path for all vertices from vertex A.
Write a paragraph to explain your work process and present the results by drawing the updated diagram after each vertex has been processed.  In each diagram, highlight the vertices that have been processed and the labels of distance at each vertex.
Question 5 (5 points) 
Apply Dijkstra’s Algorithm to the following directed graph, and compute the shortest path for all vertices from vertex A.
As in Question 5, write a paragraph to explain your progress and present your results by drawing the updated diagram after each vertex is processed. In each diagram, highlight the vertices that have been processed and the labels of distances at each vertex.
Question 6 (10 points) 
For the following graph:

(a) Apply Prim’s Algorithm, beginning at vertex A. Show the results of each stage of the algorithm.  In this case, we define a stage as the addition of a new vertex and a new edge to the MST S={V,E}.Present the results in the format of the following table (note that values provided are only examples and do not correspond to the solution), and write a paragraph to explain your work process.
Stage 
V 
E 
0 
(A) 
() 
1 
(A,B) 
((A,B)) 
. 
. 
. 
. 
. 
. 
. 
. 
. 
n 
(A,B,C.D,E,F) 
((A,B),(B,C),(C,D),(D,E),(E,F)) 
(b) Apply Kruskal’s Algorithm.  Show the results of each stage of the algorithm.  In this case, we define a stage as the processing of an edge from the graph, whether or not it is added to the MST S={V,E}.Present the results in the format of the following table (values provided are only examples and do not correspond to the solution), and write a pa代 写CS917 Foundations of Computing 2024/2025Python
代做程序编程语言ragraph to explain your work process.
Stage 
Edges 
Components 
E 
0 
((A,B), (B,C), (C,D), 
(D,E), (E,F)) 
((A), (B), (C), (D), (E), (F)) 
() 
1 
((B,C), (C,D), (D,E), 
(E,F)) 
((A,B), (C), (D), (E), (F)) 
((A,B)) 
. 
. 
. 
. 
. 
. 
. 
. 
. 
. 
. 
. 
n 

((A,B,C,D,E,F)) 
((A,B), (B,C), (C,D), 
(D,E), (E,F)) 
Note the division of the MST Vertices Set into Connected Components.
Question 7 (50 points) In Lab 2 you have learnt about Word Trees and how you can efficiently search for words, for example in a dictionary. A practical application where Word Trees are used is for efficiently searching whether ˆ(s), a fragment of a genomic sequence in an experimental sample, belongs to a particular organism.  Here we are interested in finding whether ˆ(s) can be found in one of three different Coronavirus  (SARS-Cov 2 virus) strains  (denoted as Wuhan,  Omicron, Hiroshima). You are given the gene sequence data, a string s consisting of the letters of the genetic alphabet Γ = {A,T,C, G}, of the famous S-protein (spike protein) of each strain which is an important target of different vaccination strategies.
Precisely, we are asking whether ˆ(s) is a substring of gene s. Using what is called a suffix tree of s, we can perform. a substring test for ˆ(s) in time O(|ˆ(s)|), where | ˆ(s)| is the length of ˆ(s).You will find different solutions for creating suffix trees in this context, many of which are more advanced, for example, allowing to process online data.  However, for this coursework you are meant to stick as closely to the following definition as possible. Specifically, there is no need to implement suffix links or construct an implicit tree, for example.
Definition: Simple Suffix Tree 
Let s = s1 , ..., sn  be a string.  A directed tree G =  (V, E) with a root r is called a Simple Suffix Tree for s if it satisfies the following conditions:
(i) The tree has exactly n leaves which are labelled 1, ..., n
(ii) The edges of the tree are labelled with symbols from an alphabet Γ, or $ indicating an “end” character, needed when a suffix is a prefix of another suffix
(iii) All outgoing edges  (from an inner vertex to its children) are labelled with pairwise different symbols
(iv) The path from the root to the leaf i is labelled si , ..., sn
[Hint:  (ii) becomes clear if you think about the example s = ATGATG
An example of a Simple Suffix Tree for the sequence s = TACTAG is given in Figure 1. 

Figure 1: Example of a Suffix Tree
(a) Simple Suffix Tree (25 points) Write a Python program that creates a Simple Suffix Tree according to the previous Definition, and performs a substring search.  Your program should return the start position of the substring, if found, and allow for multiple occurrences of a substring.  In Answers.pdf, provide a few examples of your choice that show that your code correctly produces a Suffix Tree.  These should be for arbitrary, short sequences, similar to the examples s  =  TACTAG or  s  =  TACTAC,  Demonstrate that you  can perform. a search successfully. You can either draw Suffix Trees by hand and take a picture, or use tools such as networkx.Your program SuffixTreeSearch.py should take three arguments:  1) a string with the filename of the file containing the sequences (for example ”Wuhan-S.txt”), 2) substringˆ(s) (for example ”AACCTTGG”), and 3) a string indicating which type of Suffix Tree to use, for Question 7a) this will be ”Simple Suffix Tree”, in 7c) this will be ”Compact Suffix Tree” . Inputs should be with quotes.
SuffixTreeSearch.py should return either: 0 (substring has not been found)
i (start index of substring ˆ(s) in s, i ∈ 1,..., n), or
multiple start indices, separated by a blank, e.g.  ”3 127 3340”, returned without quotes.You need to adhere to these conventions strictly, otherwise we cannot perform. auto-
mated tests to check the correctness of your algorithm.
(b) Substring tests for different S Proteins (10 points) Use your Suffix Tree program to search whether the following substrings are contained in the three S proteins, with the genetic sequence provided in the files Hiroshima-S.txt, Omicron-S.txt and Wuhan-S.txt.
ˆ(s)1  = ACTGAAATCTATCAG
ˆ(s)2  = ACTGAAATCTATCAGGCC
ˆ(s)3  = ACTGAAATCTATCAGGCCGGTAGC State the results in Answers.pdf.
(c) Compact Suffix Tree (15 points) Implement a Compact Suffix Tree in SuffixTreeSearch.py, recognising in Figure 1 that consecutive edges could be collapsed into a single one, with the edge providing pointers to the start and end indices of the original string.  For example, the branch labelled ”1” which has seven edges could be represented by three edges:
e1  = TA with pointers start=[1,4], end=[2,5], indicating that TA occurs twice in TACTAG, starting at the first and fourth position and ending at the second and fifth position.
e2  = G with pointers start=[6], end=[6]
e3  = CTAG with pointers start=[3], end=[6]
For genomic sequences which can be highly repetitive, for example having hundreds of ”A”s in a row, a Compact Suffix Tree can reduce memory requirements significantly.In this task you will be given a lot more flexibility.   For example, you could argue whether to maintain the $ ”end” character, or decide on different ways to use pointers. Think about borderline cases first, for example, what if s = AAAAAAAAAAAAAAAAAAA?You will be able to still score high marks in this task, if you provide a good design concept, including considerations on space complexity, even without a full implemen- tation.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
