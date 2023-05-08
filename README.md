Download Link: https://assignmentchef.com/product/solved-solvedassignment-6-binary-tree-solution
<br>
You are required to turn in the following source file(s) in C++:

Assignment6.cpp &lt;assignment6/Assignment6.cpp (No need to be modified)BinarySearchTree.h &lt;assignment6/BinarySearchTree.h (More code need tobe added)

*/_ _/*

Objectives:

-This is to practice making binary search trees.

Program Description

This is a programming assignment. You will develop a binary tree withsome of its operations.

1. You need to implement a data structure to represent a node. Each nodeshould have data fields containing course number and course title. (itskey will be course number), its parent node called “parent”, its left child node called “left”, and its right child node called “right”.

2. Using the nodes above, you need to implement a binary search treeusing their keys.

3. When you compare two nodes, compare their course numbers inalphabetical order (each character’s ASCII number).

4. Your binary search tree needs to have operations “inorderTreeWalk”,“preorderTreeWalk”, and “postorderTreeWalk”that will print all node keys in a certain order (see the lecturenotes/textbook.)

5. Your binary search tree needs to have operations “treeInsert”,“rightRotate”, “leftRotate”, “treeSearch”, “treeMinimum”, “treeMaximum”,“treeSuccessor”, and “treePredecessor”.(see the lecture notes/textbook for those operations.)

6. BinarySeachTree class should have a constructor that initializes itsroot to be NULL, and a destructor that will delete all nodes in the treeand perform garbage collections. The destructor should also print “Thenumber of nodes deleted: X” where X is the number of nodes deleted andit should be called when a user chooses to exit the program.

7. You should implement a driver class with a main method which takesthe following commands (A, B, C, D, E, F, G, H, I, J, K, Q) from thekeyboard:

A — In-order print command, it should print all keys in the tree usingthe in-order, using the following format, by placing a carriage returnbetween keys:

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE310, Course Title: Data Structures and Algorithms

It should print “tree is empty” if the tree is empty.

B — Pre-order print command, it should print all keys in the treeusing the pre-order, using the following format, by placing a carriagereturn between keys:

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE310, Course Title: Data Structures and Algorithms

It should print “tree is empty” if the tree is empty.

C — Post-order print command, it should print all keys in the treeusing the post-order, using the following format, by placing a carriagereturn between keys:

Course Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: ASU101, Course Title: The ASU Experience

It should print “tree is empty” if the tree is empty.

D — Tree Minimum command, it should call “treeMinimum” and print theminimum value as ” The first course is Course Number: XXX, Course Title:YYY ”where XXX is the course number of the first course and YYY is the coursetitle of the first course in the tree.It should print “tree is empty” if the tree is empty.

E — Tree Maximum command, it should call “treeMaximum” and print themaximum value as ” The last course is Course Number: XXX, Course Title:YYY ”where XXX is the course number of the last course and YYY is the coursetitle of the last course in the tree.It should print “tree is empty” if the tree is empty.

F — Tree Predecessor command, it should prompt “Please enter a coursenumber to find its predecessor:
”, and read in the input. It shouldcall “treePredecessor” and print the predecessor as ” The predecessor ofXXXX is Course Number: AAAA, Course Title: BBBB ” where XXXX is thecourse number entered by a user and AAAA and BBBB are the course nameand course title of the predecessor of XXXX. If it does not have anypredecessor, print “XXXX does not have any predecessor”.It should print “tree is empty” if the tree is empty.

G — Tree Successor command, it should prompt “Please enter a coursenumber to find its successor:
”, and read in the input. It should call“treeSuccessor” and print the successor as “The successor of XXXX isCourse Number: AAAA, Course Title: BBBB” where XXXX is the course numberentered by a user and AAAA and BBBB are the course name and course titleof the successor of XXXX. If it does not have any successor, print “XXXXdoes not have any successor”.It should print “tree is empty” if the tree is empty.

H — Search command, it should ask user “Please enter a course numberto search:
”.Then you should call “treeSearch” operation to search the value.Then the program should print “XXXX has course title: YYYY” if it isfound, and print “XXXX not found”, otherwise, where XXXX is the coursenumber entered by a user, and YYYY is its title.

I — Insert command, it should ask user “”Please enter acourseNumber/courseTitle to insert:
”.Then you should call “treeInsert” operation to insert this value.

Then the program should print “XXX with course title: YYY inserted” ifthe same course number does not exist in the tree, and it is insertedsuccessfully, and print “XXX with course title: YYY not inserted”,otherwise (i.e., the same course number already exists in the tree),where XXX and YYY are the course number and course title entered by a user.

J — Right Rotate command, it should ask user “Please enter acourseNumber to right-rotate:
”.Then you should call “rightRotate” operation to search its node andright-rotate around the tree around the node.

Then the program should print “Right Rotation around XXX is successful”if the course number exists in the tree, its left child exits, and itsit is right-rotated successfully, and print “Right Rotation cannot beperformed around XXX”, otherwise, where XXX is the course number enteredby a user.

K —Left Rotate command, it should ask user “Please enter acourseNumber to left-rotate:
”.Then you should call “leftRotate” operation to search its node andleft-rotate around the tree around the node.

Then the program should print “Left Rotation around XXX is successful”if the course number exists in the tree, its right child exits, and itsit is left-rotated successfully, and print “Left Rotation cannot beperformed around XXX”, otherwise, where XXX is the course number enteredby a user.

Q — Quit the program and exit. The binary search tree object should bedeleted, and it should print how many nodes are deleted.

The following is an example run.

Sample Output: (the user enters the string shown in bold)

————————————-

Choice Action—— ——A Inorder PrintB Preorder PrintC Postorder PrintD Tree MinimumE Tree MaximumF Tree PredecessorG Tree SuccessorH Tree SearchI Tree InsertJ Right RotationK Left RotationQ Quit? Display Help

What action would you like to perform?*I *Please enter a courseNumber/courseTitle to insert:Enter a course number*CSE310*Enter a course title*Data Structures and Algorithms*CSE310 with course title: Data Structures and Algorithms insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*CSE240*Enter a course title*Intro to Programming Languages*CSE240 with course title: Intro to Programming Languages insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*CSE220*Enter a course title*Programming for Computer Engineering*CSE220 with course title: Programming for Computer Engineering insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*MAT243*Enter a course title*Discrete Math Structures*MAT243 with course title: Discrete Math Structures insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*EEE120*Enter a course title*Digital Design Fundamentals*EEE120 with course title: Digital Design Fundamentals insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*PHY101*Enter a course title*Introduction To Physics*PHY101 with course title: Introduction To Physics insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*ASU101*Enter a course title*The ASU Experience*ASU101 with course title: The ASU Experience insertedWhat action would you like to perform?*A*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*B*

Course Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ASU101, Course Title: The ASU ExperienceCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*C*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: PHY101, Course Title: Introduction To PhysicsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: CSE310, Course Title: Data Structures and Algorithms

What action would you like to perform?*F*Please enter a course number to find its predecessor:*CSE240*The predecessor of CSE240 is Course Number: CSE220, Course Title:Programming for Computer Engineering

What action would you like to perform?*G*Please enter a course number to find its successor:*PHY101*PHY101 does not have any successorWhat action would you like to perform?*D*The first course is Course Number: ASU101, Course Title: The ASU Experience

What action would you like to perform?*E*The last course is Course Number: PHY101, Course Title: Introduction ToPhysics

What action would you like to perform?*H*Please enter a course number to search:*CSE220*CSE220 has course title: Programming for Computer EngineeringWhat action would you like to perform?*H*Please enter a course number to search:*EEE120*EEE120 has course title: Digital Design FundamentalsWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*FSE100*Enter a course title*Introduction to Engineering*FSE100 with course title: Introduction to Engineering insertedWhat action would you like to perform?*I*Please enter a courseNumber/courseTitle to insert:Enter a course number*ENG200*Enter a course title*Critical Reading &amp; Writing About Literature*ENG200 with course title: Critical Reading &amp; Writing About LiteratureinsertedWhat action would you like to perform?*H*Please enter a course number to search:*FSE100*FSE100 has course title: Introduction to EngineeringWhat action would you like to perform?*J*Please enter a courseNumber to right-rotate:*CSE310*Right Rotation around CSE310 is successfulWhat action would you like to perform?*A*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*B*

Course Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*C*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: PHY101, Course Title: Introduction To PhysicsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: CSE240, Course Title: Intro to Programming Languages

What action would you like to perform?*K*Please enter a courseNumber to left-rotate:*EEE120*Left Rotation around EEE120 is successfulWhat action would you like to perform?*A*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*B*

Course Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*C*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: PHY101, Course Title: Introduction To PhysicsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: CSE240, Course Title: Intro to Programming Languages

What action would you like to perform?*F*Please enter a course number to find its predecessor:*PHY102*PHY102 does not have any predecessorWhat action would you like to perform?*G*Please enter a course number to find its successor:*CSE310*The successor of CSE310 is Course Number: EEE120, Course Title: DigitalDesign Fundamentals

What action would you like to perform?*D*The first course is Course Number: ASU101, Course Title: The ASU Experience

What action would you like to perform?*E*The last course is Course Number: PHY101, Course Title: Introduction ToPhysics

What action would you like to perform?*A*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*B*

Course Number: CSE240, Course Title: Intro to Programming LanguagesCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: PHY101, Course Title: Introduction To Physics

What action would you like to perform?*C*

Course Number: ASU101, Course Title: The ASU ExperienceCourse Number: CSE220, Course Title: Programming for Computer EngineeringCourse Number: ENG200, Course Title: Critical Reading &amp; Writing AboutLiteratureCourse Number: EEE120, Course Title: Digital Design FundamentalsCourse Number: FSE100, Course Title: Introduction to EngineeringCourse Number: PHY101, Course Title: Introduction To PhysicsCourse Number: MAT243, Course Title: Discrete Math StructuresCourse Number: CSE310, Course Title: Data Structures and AlgorithmsCourse Number: CSE240, Course Title: Intro to Programming Languages

What action would you like to perform?*Q*The number nodes deleted: 9

———————————————-

*Implementation/Documentation Requirements:*

* You need to implement this program using C++ and it has to read fromthe standard input (from a keyboard).* Your program needs to compile and execute in general.asu.edu.* Your code should be well documented and commented.* You must use the provided data sets.* Also you are not allowed to use any predefined data structures (suchas ones in the library in C++, etc.), you need to build your owndata structures and operations associated with them (such as Insertor Search).* Copying any codes from other people’s programs is considered to becheating and will lead to a report to the Dean and you will bepenalized.

*What to turn in:*

You must turn in C++ source code using the following submission site:

http://courses.eas.asu.edu/cse310/

First, you need to login, and click on the *Submission* page. You needto select the correct assignment number. The types of files that you cansubmit are .cpp, or .h files. They have to compile and execute in*/general.asu.edu/* server. (You can access general.asu.edu by SSH, andlogin using your ASU UserID and password.)

For C++, the files need to compile and execute with the commands:

/ /

/g//++ *.cpp/

/ /

/./a.out/

You program should be well commented and documented, make sure the firstfew lines of your program contain your name, your ASU email address, anda description of each file. While you will not be graded on styletechnique (“i++” or “i = i + 1”) or indenting by 4 spaces or tables, youshould use indentation, good variable names, and clear, easy to read,and specific comments. (You will be graded on comments.)

Input

The following files are sample test cases that will be used as input foryour program (Right-click and use “Save As”):

Test Case #1 &lt;assignment6/input1.txtTest Case #2 &lt;assignment6/input2.txtTest Case #3 &lt;assignment6/input3.txt

Sample output for the input1.txt

Test Case #1 &lt;assignment6/output1.txt

You can test your program as follows:

For a C++ program, after compiling your files, one way is:

/./a.out//&lt; input1.txt/

or you can replace a.out with whichever your executable is.

Error Handling

Your program will be tested with other input besides the ones above,thus is expected to be robust.