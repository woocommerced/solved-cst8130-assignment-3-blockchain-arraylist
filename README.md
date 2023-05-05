Download Link: https://assignmentchef.com/product/solved-cst8130-assignment-3-blockchain-arraylist
<br>
In this assignment, you will expand on Lab 4/ 5’s implementation of BlockChain in two ways:  <strong>moving</strong> it <strong>to</strong> using the Java <strong>Linked List class</strong>, and <strong>making</strong> a <strong>collection</strong> of BlockChains in an <strong>ArrayList</strong>.

Note – you may use my posted solution for Lab 5 to begin if you find that helpful.    I suggest that you implement the changes in the order that I have listed below – so <strong>get (a)</strong> changes working….then <strong>add (b).</strong>

<ol>

 <li>The BlockChain class will be revised to use the LinkedList java class (instead of keeping head/tail and doing all the linked list programming ourselves, we will use the LinkedList methods). So – the data members in BlockChain class will now be:</li>

</ol>

private  LinkedList &lt;Block&gt; blockChain;

private String courseName;

The <strong>methods</strong> will need to be <strong>rewritten</strong>.

Note – this will mean a change to the Block class in that you will need to remove the nextOne field in that class and update the methods appropriately. The currentHash and previousHash fields in this class still must be handled by us in our code.   (The LinkedList class in Java now looks after only the link to the next Block).

<ol>

 <li>Add a College class to this project whose data members will be</li>

</ol>

private ArrayList&lt;BlockChain&gt; college;

private String collegeName;

Note that each BlockChain is actually representing the grades in a course. (so we could  have changed  the BlockChain class  name to CourseGrades).

The menu for the main method will have the following options:

<ul>

 <li>Display the courses (and their corresponding data) – for each of the <strong>BlockChains (courses)</strong> in the college ArrayList</li>

 <li>Add a new course</li>

 <li>Add a new block (then user will be prompted which course to add the block to)</li>

 <li>Add a bad block (artificial – but we will keep this so we can have bad blocks)</li>

 <li>Verify college – verify each of the BlockChains in the college ArrayList</li>

</ul>

Note – in my sample output below, I did not test all error conditions – but you must do this in your program (and then write a test plan for only the changes made in this program).

<strong><em>Sample Output: (green is user input)</em></strong>

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

1

For college: Algonquin

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

2

Enter name of course to add:

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

1

For college: Algonquin

For course: CST8130

[

0 100 2152018 current: 24455.0 previous: 0.0]

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

3

Enter which course to add :

0 CST8130:

0

Add good block or bad?  (g for good, anything else for bad):

g

Enter date: 2282018

Enter student number: 1234

Enter grade:

87

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

1

For college: Algonquin




For course: CST8130

[

0 100 2152018 current: 24455.0 previous: 0.0,

1234 87 2282018 current: 25947.0 previous: 24455.0]

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

2

Enter name of course to add:

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

3

Enter which course to add :

0 CST8130:

1 CST8110:

Add good block or bad?  (g for good, anything else for bad):

Enter date: 2282018

Enter student number: 54321

Enter grade:

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

2

Enter name of course to add:

CST888

Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

3

Enter which course to add :

0 CST8130:

1 CST8110:

2 CST8888:

2

Add good block or bad?  (g for good, anything else for bad):

b

Enter date: 2282018

Enter student number: 12341234

Enter grade:

88




Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

1

For college: Algonquin




For course: CST8130

[

0 100 2152018 current: 24455.0 previous: 0.0,

1234 87 2282018 current: 25947.0 previous: 24455.0]




For course: CST8110

[

0 100 2152018 current: 24455.0 previous: 0.0,

54321 66 2282018 current: 26550.0 previous: 24455.0]




For course: CST8888

[

0 100 2152018 current: 24455.0 previous: 0.0,

12341234 88 2282018 current: 166174.0 previous: 0.10431117]







Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

4

Chain for CST8130 is verified

Chain for CST8110 is verified

Chain for CST8888 is not verified




Enter 1 to display the college courses:

2 to add a new course:

3 to add a block:

4 to verify chains:

5 to fix a chain:

6 to quit:

5

Enter which course to fix:

0 CST8130:

1 CST8110:

2 CST8888:

3

Invalid entry:  please reenter:

2

Chain is fixed.


