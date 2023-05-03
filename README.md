Download Link: https://assignmentchef.com/product/solved-cs161-fundamentals-of-artificial-intelligence-assignment-1
<br>
<h1>Questions</h1>

<ol>

 <li>This problem concerns the Padovan sequence. The first few elements of the sequence are 1 1 1 2 2 3 4</li>

</ol>

5 7 9 12 16 21, …. The sequence is defined as

PAD(<em>n </em>+ 1) = PAD(<em>n </em>− 1) + PAD(<em>n </em>− 2)

with

PAD(0) = PAD(1) = PAD(2) = 1<em>.</em>

Write a single LISP function, called PAD, that takes a single integer argument N, and returns the <em>N</em>th Padovan number. For example (PAD 5) returns 3, (PAD 3) returns 2, and (PAD 4) returns 2.

Test your program on at least the first 10 Padovan numbers. Also test your program for larger values of N. What happens? Explain why in your <strong>hw1.txt </strong>file.

<ol start="2">

 <li>Write a single LISP function, called SUMS, that takes a single numeric argument N, and returns the number of additions required by your PAD function to compute the <em>N</em>th Padovan number. SUMS should not call PAD, but rather you should design the recursion for SUMS by examining your PAD</li>

</ol>

Test your program on at least the first 10 values. What is the relationship between the values returned by PAD and SUMS? Explain why in you <strong>hw1.txt </strong>file.

<ol start="3">

 <li>A tree can be represented in LISP as follows:

  <ul>

   <li>if the tree contains a single leaf node <em>L</em>, it can be represented by atom L</li>

   <li>if the tree has more than one node and is rooted at <em>N</em>, then it can be represented by a list (S1 S2 … Sk) where Si represents the <em>i</em>th subtree of <em>N</em>.</li>

  </ul></li>

</ol>

Consider for example the following five trees.

-0.2

1-0.2

foo 3.1

l      e                                                                                                       1

Their LISP representations are respectively (((l e ) f ) t ), (5 foo 3.1 -0.2), (1 (foo 3.1) -0.2), ( ((1 2) (foo 3.1)) (bar -0.2)), and (r ( i ( g ( h t)))).

Write a single LISP function, called ANON. It takes a single argument TREE that represents a tree, and returns an anonymized tree with the same structure, but where all symbols and numbers in the tree are replaced by a question mark. The anonymized versions of the trees above are as follows.

?      ?      ?      ?

?                                                                                            ???

?                                  ??

?      ?                                                                                                   ?      ?      ?      ?

?      ?

Test your program on at least these inputs:

&gt; (ANON ’42) ?

&gt; (ANON ’FOO) ?

&gt; (ANON ’(((L E) F) T))

(((? ?) ?) ?)

&gt; (ANON ’(5 FOO 3.1 -0.2))

(? ? ? ?)

&gt; (ANON ’(1 (FOO 3.1) -0.2))

(? (? ?) ?)

&gt; (ANON ’(((1 2) (FOO 3.1)) (BAR -0.2)))

(((? ?) (? ?)) (? ?))

&gt; (ANON ’(R (I (G (H T))))) (? (? (? (? ?))))


