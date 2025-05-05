# cse340-17-project-2-solved
**TO GET THIS SOLUTION VISIT:** [CSE340 17 Project 2 Solved](https://www.ankitcodinghub.com/product/cse340-17-project-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;34050&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;6&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (6 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE340 17 Project 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (6 votes)    </div>
    </div>
<h1>1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Introduction</h1>
In this project, you will write a C or C++ program that reads a description of a context free grammar, then, depending on the command line argument passed to the program, performs one of the following tasks: 1) for each terminal and non-terminal in the grammar determine the number of grammar rules in which the symbol appears, 2) determine <em>useless </em>symbols in the grammar and remove them, 3) calculate FIRST sets, 4) calculate FOLLOW sets and 5) determine if the grammar has a predictive parser.

<h1>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Input Format</h1>
We specify the input format using a context-free grammar:

Rule-list <em>→ </em>Rule Rule-list <em>| </em>Rule

Id-list <em>→ </em>ID Id-list <em>| </em>ID

Rule <em>→ </em>ID ARROW Right-hand-side HASH Right-hand-side <em>→ </em>Id-list <em>| </em>

The tokens used in the above grammar description are defined by the following regular expressions:

ID&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = letter (letter + digit)*

HASH&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = #

DOUBLEHASH = ##

ARROW&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = -&gt;

Where digit is the digits from 0 through 9 and letter is the upper and lower case letters a through z and A through Z. Tokens are case-sensitive. Tokens are space separated and there is at least one whitespace character between any two successive tokens.

<h1>3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Semantics</h1>
Each grammar rule starts with a non-terminal symbol (the left-hand side of the rule) followed by ARROW, then followed by a sequence of zero or more terminals and non-terminals, which represent the right-hand side of the rule. If the sequence of terminals and non-terminals in the right-hand side is empty, then it represents a rule of the form A <em>→ </em>.

The set of non-terminals for the grammar is the set of symbols that appear to the left of an arrow. Grammar symbols that do not appear to the left of an arrow are terminal symbols.

Note that the convention of using upper-case letters for non-terminals and lower-case letters for terminals is not used here.

<h2>3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Example</h2>
Here is an example input:

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

##

The non-terminals of the grammar are:

Non-Terminals = <em>{</em>decl<em>,</em>idList1<em>,</em>idList<em>}</em>

The terminals of the grammar are:

Terminals = <em>{</em>ID<em>,</em>COMMA<em>,</em>colon<em>}</em>

and the grammar rules are:

decl <em>→ </em>idList colon ID

idList <em>→ </em>ID idList1

idList1 <em>→&nbsp; </em>idList1 <em>→ </em>COMMA ID idList1

Note that even though the example shows that each rule is on a line by itself, a rule can be split into multiple lines, or even multiple rules can be on the same line, according to the formal specification. The following input describes the same grammar as the above example:

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1

-&gt; COMMA ID idList1 #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ##

<h1>4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Output Specifications</h1>
Your program should read the input grammar from standard input, and read the requested task number from the first command line argument (we provide code to read the task number) then calculate the requested output based on the task number and print the results in the specified format for each task to standard output (stdout). The following specifies the exact requirements for each task number.

<h2>4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Task 1</h2>
Task one simply outputs the list of terminals followed by the list of non-terminals in the order in which they appear in the grammar rules.

<strong>Example:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>For the input grammar

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

## the expected output for task 1 is: colon ID COMMA decl idList idList1

<strong>Example:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Given the input grammar:

decl -&gt; idList colon ID # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 # idList -&gt; ID idList1 #

## the expected output for task 1 is:

colon ID COMMA decl idList idList1

Note that in this example, even though the rule for idList1 is before the rule for idList, idList appears before idList1 in the grammar rules.

<h2>4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Task 2: Find useless symbols</h2>
Determine <em>useless </em>symbols in the grammar and remove them. Then output each rule of the modified grammar on a single line in the following format:

&lt;LHS&gt; -&gt; &lt;RHS&gt;

Where &lt;LHS&gt; should be replaced by the left-hand side of the grammar rule and &lt;RHS&gt; should be replaced by the right-hand side of the grammar rule. If the grammar rule is of form <em>A → </em>, use # to represent the epsilon. Note that this is different from the input format. Also note that the order of grammar rules that are not removed from the original input grammar must be preserved.

<strong>Definition: </strong>Symbol <em>A </em>is <em>not </em>useless if there is a derivation starting from <em>S </em>(the start symbol) in which <em>A </em>appears and the derivation leads to a string of terminals <em>w </em>or the empty string (<em>w ∈ T<sup>∗</sup></em>):

<em>∗&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ∗</em>

<em>S ⇒ …A… ⇒ w</em>

<strong>Example 1:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Given the following input grammar :

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

## the expected output for task 2 is:

decl -&gt; idList colon ID idList -&gt; ID idList1 idList1 -&gt; # idList1 -&gt; COMMA ID idList1

Note that none of the symbols were useless.

<strong>Example 2:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Given the following input grammar:

S -&gt; A B #

S -&gt; C #

C -&gt; c #

S -&gt; a #

<ul>
<li>-&gt; a A #</li>
<li>-&gt; b #</li>
</ul>
## the expected output for task 2 is:

S -&gt; C

C -&gt; c

S -&gt; a

Note that A and B are useless symbols and the modified grammar has only three rules.

<h2>4.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Task 3: Calculate FIRST Sets</h2>
For each of the non-terminals of the input grammar, in the order that they appear in grammar, compute the FIRST set for that non-terminal and output one line in the following format:

FIRST(&lt;symbol&gt;) = { &lt;set_items&gt; }

Where &lt;symbol&gt; should be replaced by the non-terminal and &lt;set_items&gt; should be replaced by the comma-separated list of elements of the set ordered in the following manner:

<ul>
<li>If belongs in the set, represent it as #</li>
<li>If belongs in the set, it should be listed before any other elements</li>
<li>All other elements of the set should be sorted in the order in which they appear in the terminal list (first section of the input)</li>
</ul>
<strong>Example:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Given the input grammar:

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

## the expected output for task 3 is:

FIRST(decl) = { ID }

FIRST(idList1) = { #, COMMA }

FIRST(iDList) = { ID }

<h2>4.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Task 4: Calculate FOLLOW Sets</h2>
For each of the non-terminals of the input grammar, in the order that they appear in the nonterminals section of the input, compute the FOLLOW set for that non-terminal and output one line in the following format:

FOLLOW(&lt;symbol&gt;) = { &lt;set_items&gt; }

Where &lt;symbol&gt; should be replaced by the non-terminal and &lt;set_items&gt; should be replaced by the comma-separated list of elements of the set ordered in the following manner:

<ul>
<li>If EOF belongs in the set, represent it as $</li>
<li>If EOF belongs in the set, it should be listed before any other elements</li>
<li>All other elements of the set should be sorted in the order in which they appear in the terminal list (first section of the input)</li>
</ul>
<strong>Example:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>Given the input grammar:

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

## the expected output for task 3 is:

decl -&gt; idList colon ID # idList -&gt; ID idList1 # idList1 -&gt; # idList1 -&gt; COMMA ID idList1 #

##

FOLLOW(decl) = { $ }

FOLLOW(idList1) = { colon }

FOLLOW(idList) = { colon }

<h2>4.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Task 5: Determine if the grammar has a predictive parser</h2>
Determine if the grammar has a predictive parser and output either YES or NO accordingly.

<strong>Example:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong>The expected output for the example input grammar given in section 3.1 for task 5 is:

YES

<h1>5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Implementation</h1>
<h2>5.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Lexer</h2>
A lexer that can recognize ID, ARROW, HASH and DOUBLEHASH tokens is provided for this project. You are free to use it if you like.

<h2>5.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Reading command-line argument</h2>
As mentioned in the introduction, your program must read the grammar from stdin and the task number from command line arguments. The following piece of code shows how to read the first command line argument and perform a task based on the value of that argument. Use this code as a starting point for your main function.

/* NOTE: You should get the full version of this code as part of the project material, do not copy/paste from this document. */

#include &lt;stdio.h&gt; #include &lt;stdlib.h&gt;

int main (int argc, char* argv[])

{ int task;

if (argc &lt; 2) {

printf(“Error: missing argument\n”); return 1;

} task = atoi(argv[1]);

switch (task) { case 1:

// TODO: perform task 1. break; // …

default: printf(“Error: unrecognized task number %d\n”, task); break;

} return 0;

}

<h1>6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Evaluation</h1>
Your submission will be graded on passing the automated test cases. The test cases (there will be multiple test cases in each category, each with equal weight) will be broken down in the following way (out of 100 points):

<ul>
<li>Task 1: 10 points</li>
<li>Task 2: 30 points</li>
<li>Task 3: 30 points</li>
<li>Task 4: 25 points</li>
<li>Task 5: 5 points</li>
</ul>
Submit your code on the course submission website: <a href="http://cse340.fulton.asu.edu/cse340/">http://cse340.fulton.asu.edu/cse340/</a>
