Download Link: https://assignmentchef.com/product/solved-cs300-homework-2-notebook
<br>



In this homework, you will implement two “Notebooks” by using the AVL Search Tree and the Binary Search Tree (BST). Additionally, you will display the speed of some of the operations on these tree data structures that are used for the implementation. Each “Notebook” will have a nested tree structure, which will be explained in more detail in the rest of the documentation.

Although each Notebook tree will have a separate implementation, they will store the same data and will perform the same operations. Basically, the only difference between the Notebooks will be the data structures that are going to be used for the implementation. Each Notebook will contain multiple <em>sections</em> and each <em>section</em> will have multiple <em>items</em> which will store the information inside.

A notebook will have a nested structure as follows:




<ul>

 <li><strong>Notebook</strong></li>

</ul>

May have one or many <strong>section</strong>/s.

<ul>

 <li><strong>Section</strong></li>

</ul>

Will have a <strong>title</strong>.

May have one or many <strong>item</strong>/s.

<ul>

 <li><strong>Item</strong></li>

</ul>

Will have a <strong>title</strong>.

Will have information.

<u> </u>

<u>Example Notebook:</u>

<u> </u>

Courseworks

CS300-the homework is due Sunday

CS408-don’t forget the quiz

CS303-16:40 office hour

Movies

The Holy Mountain-7.9

I Lost My Body-7.6

Phonebook

Gulsen-09990000099

Alp-09998765432

Furkan-09876543210

Serra-09898989898







As seen in the example above, <u>a notebook is a tree of sections</u>. Each section has got a <u>title string</u> and <u>a tree of items</u>. Each item has <u>a title string</u> and <u>an information string</u>.

There cannot be two sections with the same title <u>inside the same notebook</u>. Also, there cannot be two items with the same title <u>inside the same section</u>.




<strong> </strong>

<strong>BST and AVL Tree</strong>

<strong> </strong>

You are going to implement a BST class and an AVL Tree class. Which will get used separately to implement two different notebooks that will perform the same operations over the same data. You <strong><u>CANNOT</u></strong><strong> USE VECTOR OR ARRAY</strong> to implement the notebooks. Also, you <strong><u>cannot</u> use a BST inside an AVL Tree and vice versa</strong>. In other words, there will be two notebooks, one of them will be implemented by using nested AVL Trees and the other will get implemented by using the nested BSTs only.




Both the BST and the AVL Tree classes should be reusable for different types, classes, etc. Thus, both the BST and AVL Tree classes <strong><u>MUST</u></strong> be <strong><u>template-based</u> </strong>classes.




<u>Use the “<strong>title”</strong> properties of the section and the item to compare the nodes inside the trees.</u>

<strong> </strong>

<strong> </strong>

<strong>Program Flow</strong>

<strong> </strong>

<ul>

 <li><strong>Initializing the notebooks</strong></li>

</ul>

At the very beginning of the program, you should create two notebooks (one by using the BST, other by using the AVL Tree).




Then, your program will read a text file that contains the section and item data of the notebook. Your program will insert the data into the notebooks accordingly.




Your program will display the elapsed insertion time of each section for both of the notebooks. Then the program will direct to the main menu.




<strong> </strong>

<ul>

 <li><strong>Main menu</strong></li>

</ul>

On the main menu, there will be 6 options. The user will enter an input between [1-6] then the program will perform the commands on both notebooks accordingly. These options are:

<ol>

 <li><u>Display the sections (AVL)</u></li>

</ol>

Your program should perform an inorder traversal over the AVL notebook and print the section titles in ascending order (alphabetically).

<ol start="2">

 <li><u>Display the sections (BST)</u></li>

</ol>

Your program should perform an inorder traversal over the BST notebook and print the section titles in ascending order (alphabetically).

<ol start="3">

 <li><u>Select a section</u></li>

</ol>

The program will get a section title name from the user then it will search for the section with the same title, both in the AVL and BST notebooks.

If there exists no such section your program will display an error. Else it will direct to the <strong>section menu </strong>to perform operations on the selected section.




<ol start="4">

 <li><u>Add new section</u></li>

</ol>

Get a title input from the user. If a section with the given title already exists in the notebook, display an error message. Else, create a new section with that title and insert it into the notebooks.

<ol start="5">

 <li><u>Delete a section</u></li>

</ol>

Get a title input from the user. If a section with the given title does not exist in the notebook, display an error message. Else, remove the section with that title from the notebooks.

<ol start="6">

 <li><u>Exit</u></li>

</ol>

Terminate the program.







<ul>

 <li><strong>Section menu</strong></li>

</ul>

At option 3 of the main page, if the title of any section matches with the input from the user, the program should land on the section menu page to perform operations on the selected section.




On the main menu, there will be 7 options. The user will enter an input between [1-7] then the program will perform the commands on both notebooks accordingly. Options are:




<ol>

 <li><u>Display the items (AVL)</u></li>

</ol>

For the selected section of the AVL notebook:

Your program should perform an inorder traversal over the items tree of the section and print the item titles in ascending order (alphabetically).

<ol start="2">

 <li><u>Display the items (BST)</u></li>

</ol>

For the selected section of the BST notebook:

Your program should perform an inorder traversal over the items tree of the section and print the item titles in ascending order (alphabetically).

<ol start="3">

 <li><u>Display the information of an item</u></li>

</ol>

Get an item title input from the user. If an item with the given title does not exist in the notebook, display an error message. Else, display the information of the matching item.




Note: Although, you should make a query on both the AVL notebook and the BST notebook you can display the matching item information once. Since, if your program works correctly, matching item information of the AVL notebook and the BST notebook will be the same.




In both cases, display the elapsed query/insertion time for the AVL notebook and the BST notebook.

Display the elapsed query time.




<ol start="4">

 <li><u>Add a new item</u></li>

</ol>

Get an item title input from the user. If an item with the given title already exists in the section, display an error message. Else, create a new item with that title and insert it into the selected section.

In both cases, display the elapsed query/insertion time.

<ol start="5">

 <li><u>Update the information of an item:</u></li>

</ol>

Get an item title input from the user. If an item with the given title does not exist in the section, display an error message. Else, get the new information from the user and update the information of the item accordingly.

Display the elapsed query/update time.

<ol start="6">

 <li><u>Delete an item</u></li>

</ol>

Get an item title input from the user. If an item with the given title does not exist in the section, display an error message. Else, remove the item with that title from the section. Display the elapsed deletion time.

<ol start="7">

 <li><u>Return to main menu</u></li>

</ol>

Go back to the main menu.




<strong>Text File</strong>

As mentioned before we have provided initial data to fill the notebooks at the beginning of the program. You should read the data from a text file (.txt extension) and insert it into the notebooks accordingly.




The text file will contain the following 3 sections:




<ul>

 <li><u>Courseworks:</u> contains 5 non-sorted items.</li>

 <li><u>Movies:</u> contains +90000 non-sorted items.</li>

 <li><u>Phonebook:</u> contains +6000 <strong>sorted</strong></li>

</ul>




<ul>

 <li><strong>Data format</strong></li>

</ul>

If the first character of a line is not a ‘-‘ (dash), it is the title of a new section. Until the occurrence of a new section, as long as a new line starts with a dash it denotes the item of the given section. Each item line contains exactly two dashes. The first one denotes that it is an item line and the second one separates the item title from the item info.




So, a text file with notebook data inside it will look like the following:

Section title 1

-item title 1-item info 1

-item title 2-item info 2

-item title 3-item info 3

Section title 2

-item title 1-item info 1

-item title 2-item info 2







Example text file:




Courseworks

-CS300-the homework is due Sunday

-CS408-don’t forget the quiz

-CS303-16:40 office hour

Movies

-The Holy Mountain (1973)-7.9

-Climax-7

-Midsommar-7.6

<strong> </strong>

<strong> </strong>

<strong>Elapsed Time</strong>

<strong> </strong>

You should display the elapsed time of the notebook operations. For that purpose, you can use the C++ built-in library <strong>chrono</strong>. You can include the library by using #include &lt;chrono&gt;.




You are recommended to use <strong>chrono::high_resolution_clock</strong> to obtain accurate results.

Documentation: <a href="https://en.cppreference.com/w/cpp/chrono/high_resolution_clock">https://en.cppreference.com/w/cpp/chrono/high_resolution_clock</a>




Here is an example to get the time duration of a foo() function in microseconds:

<strong> </strong>

<strong>Between the start and the end clocks, you should only include the member functions of the trees (insert, delete, update, etc.) and exclude the rest of the code (getline, loops, arithmetic operations, etc.).</strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Sample Run</strong>

<strong> </strong>

Welcome to the the Notes




Section “Courseworks” has been inserted into the AVL notebook.

[AVL] Elapsed time: 15 microseconds

Section “Courseworks” has been inserted into the BST notebook.

[BST] Elapsed time: 7 microseconds




Section “Phonebook” has been inserted into the AVL notebook.

[AVL] Elapsed time: 18236 microseconds

Section “Phonebook” has been inserted into the BST notebook.

[BST] Elapsed time: 3864642 microseconds




Section “Movies” has been inserted into the AVL notebook.

[AVL] Elapsed time: 300933 microseconds

Section “Movies” has been inserted into the BST notebook.

[BST] Elapsed time: 353231 microseconds




MENU

Please enter an input between [1 – 6]:

1- Display the sections [AVL]

2- Display the sections [BST]

3- Select a section

4- Add new section

5- Delete a section

6- Exit

Input: <strong>1</strong>




*****

Courseworks

Movies

Phonebook

*****




Input: <strong>2</strong>




*****

Courseworks

Movies

Phonebook

*****




Input: <strong>3</strong>

Enter the title of the section: <strong>Cour</strong>

Invalid title!




Input: <strong>3</strong>

Enter the title of the section: <strong>Courseworks</strong>




Selected section -&gt; Courseworks

Please enter an input between [1 – 7]:

1- Display the items [AVL]

2- Display the items [BST]

3- Display the information of a item

4- Add new item

5- Update the information of a item

6- Delete an item

7- Return to main menu

Input: <strong>1</strong>

<strong> </strong>

*****

CS300

CS303

CS408

ENS492

SPS303

*****




Input: <strong>2</strong>




*****

CS300

CS303

CS408

ENS492

SPS303

*****




Input: <strong>3</strong>

Enter the title of the item: <strong>CS100</strong>

[AVL] Elapsed time: 8 microseconds

[BST] Elapsed time: 2 microseconds

Invalid title.




Input: <strong>3</strong>

Enter the title of the item: <strong>CS300</strong>

[AVL] Elapsed time: 6 microseconds

[BST] Elapsed time: 0 microseconds

the homework is due Sunday




Input: <strong>4</strong>

Enter a title for the item: <strong>CS303</strong>

Item “CS303” already exists in the “Courseworks”.




Input:<strong> 4</strong>

Enter a title for the item: <strong>CS600</strong>

Enter a description for the item: <strong>huh?</strong>

[AVL] Elapsed time: 14 microseconds

[BST] Elapsed time: 3 microseconds

The new item “CS600” has been inserted.




Input: <strong>5</strong>

Enter the title of the item: <strong>CS999</strong>

[AVL] Elapsed time: 5 microseconds

[BST] Elapsed time: 2 microseconds

Item “CS999” does not exist in the “Courseworks”.




Input: <strong>5</strong>

Enter the title of the item: <strong>CS300</strong>

[AVL] Elapsed time: 6 microseconds

[BST] Elapsed time: 0 microseconds

Enter the new information: <strong>great</strong>

The content CS300 has updated.




Input: <strong>3</strong>

Enter the title of the item: <strong>CS300</strong>

[AVL] Elapsed time: 7 microseconds

[BST] Elapsed time: 1 microseconds

great




Input: <strong>6</strong>

Enter the title of the item: <strong>CS123</strong>

Item “CS123” does not exist in the “Courseworks”.




Input: <strong>6</strong>

Enter the title of the item: <strong>CS300</strong>

[AVL] Elapsed time: 2 microseconds

[BST] Elapsed time: 2 microseconds

The item “CS300” has been deleted.




Input: <strong>1</strong>




*****

CS303

CS408

CS600

ENS492

SPS303

*****




Input: <strong>2</strong>




*****

CS303

CS408

CS600

ENS492

SPS303

*****




Input: <strong>7</strong>




MENU

Please enter an input between [1 – 6]:

1- Display the sections [AVL]

2- Display the sections [BST]

3- Select a section

4- Add new section

5- Delete a section

6- Exit

Input: <strong>4</strong>

Enter a title for the section: <strong>Courseworks</strong>

Section “Courseworks” already exists.




Input: <strong>4</strong>

Enter a title for the section: <strong>Colors</strong>

The new section “Colors” has been inserted.




Input: <strong>3</strong>

Enter the title of the section: <strong>Colors</strong>




Selected section -&gt; Colors

Please enter an input between [1 – 7]:

1- Display the items [AVL]

2- Display the items [BST]

3- Display the information of a item

4- Add new item

5- Update the information of a item

6- Delete an item

7- Return to main menu

Input: <strong>1</strong>




*****

*****




Input: <strong>2</strong>




*****

*****




Input: <strong>4</strong>

Enter a title for the item: <strong>Red</strong>

Enter a description for the item: <strong>Fav</strong>

[AVL] Elapsed time: 4 microseconds

[BST] Elapsed time: 1 microseconds

The new item “Red” has been inserted.




Input: <strong>1</strong>




*****

Red

*****




Input: <strong>2</strong>




*****

Red

*****




Input: <strong>7</strong>




MENU

Please enter an input between [1 – 6]:

1- Display the sections [AVL]

2- Display the sections [BST]

3- Select a section

4- Add new section

5- Delete a section

6- Exit

Input:<strong> 1</strong>




*****

Colors

Courseworks

Movies

Phonebook

*****




Input: <strong>2</strong>




*****

Colors

Courseworks

Movies

Phonebook

*****




Input: <strong>5</strong>

Enter the title of the section: <strong>Course</strong>

Section “Course” does not exist.




Input: <strong>5</strong>

Enter the title of the section: <strong>Courseworks</strong>

The section has been deleted.




Input:<strong> 1</strong>




*****

Colors

Movies

Phonebook

*****




Input:<strong> 2</strong>




*****

Colors

Movies

Phonebook

*****




Input:<strong> 3</strong>

Enter the title of the section: <strong>Phonebook</strong>




Selected section -&gt; Phonebook

Please enter an input between [1 – 7]:

1- Display the items [AVL]

2- Display the items [BST]

3- Display the information of a item

4- Add new item

5- Update the information of a item

6- Delete an item

7- Return to main menu

Input: <strong>3</strong>

Enter the title of the item: <strong>Aada</strong>

[AVL] Elapsed time: 2465 microseconds

[BST] Elapsed time: 0 microseconds

0016839979200




Input: <strong>3</strong>

Enter the title of the item:<strong> Zyrie</strong>

[AVL] Elapsed time: 2302 microseconds

[BST] Elapsed time: 2276 microseconds

0017707501460




Input: <strong>5</strong>

Enter the title of the item: <strong>Zyrie</strong>

[AVL] Elapsed time: 2410 microseconds

[BST] Elapsed time: 2327 microseconds

Enter the new information: <strong>000000</strong>

The content Zyrie has updated.




Input: <strong>6</strong>

Enter the title of the item: <strong>Kadeem</strong>

[AVL] Elapsed time: 6 microseconds

[BST] Elapsed time: 878 microseconds

The item “Kadeem” has been deleted.




Input: <strong>4</strong>

Enter a title for the item: <strong>Zxxy</strong>

Enter a description for the item:<strong> ???</strong>

[AVL] Elapsed time: 12 microseconds

[BST] Elapsed time: 2143 microseconds

The new item “Zxxy” has been inserted.




Input: <strong>7</strong>




MENU

Please enter an input between [1 – 6]:

1- Display the sections [AVL]

2- Display the sections [BST]

3- Select a section

4- Add new section

5- Delete a section

6- Exit

Input: <strong>3</strong>

Enter the title of the section: <strong>Movies</strong>




Selected section -&gt; Movies

Please enter an input between [1 – 7]:

1- Display the items [AVL]

2- Display the items [BST]

3- Display the information of a item

4- Add new item

5- Update the information of a item

6- Delete an item

7- Return to main menu

Input: <strong>3</strong>

Enter the title of the item:<strong> Zingaresca</strong>

[AVL] Elapsed time: 31739 microseconds

[BST] Elapsed time: 2 microseconds

6.6

<strong> </strong>

Input: <strong>5</strong>

Enter the title of the item: <strong>Aurora</strong>

[AVL] Elapsed time: 30734 microseconds

[BST] Elapsed time: 2 microseconds

Enter the new information: <strong>cool</strong>

The content Aurora has updated.




Input: <strong>6</strong>

Enter the title of the item: <strong>Redskin</strong>

[AVL] Elapsed time: 8 microseconds

[BST] Elapsed time: 1 microseconds

The item “Redskin” has been deleted.




Input: <strong>7</strong>




MENU

Please enter an input between [1 – 6]:

1- Display the sections [AVL]

2- Display the sections [BST]

3- Select a section

4- Add new section

5- Delete a section

6- Exit

Input: <strong>6</strong>

<strong> </strong>

<strong>Terminating…</strong>

<strong>Program ended with exit code: 0</strong>

<strong> </strong>

<strong>General Rules and Guidelines about Homeworks</strong>

The following rules and guidelines will apply to all homework unless otherwise noted.

<strong>How to get help?</strong>

You may ask questions to TAs (Teaching Assistants) of CS300. Office hours of TAs can be found <a href="https://docs.google.com/spreadsheets/d/1j1iKOuzwXQ-e-kuCWcOA6OJtUVD8JVQdIFqosiUerRY/edit#gid=0">here</a>. Recitations will partially be dedicated to clarifying the issues related to homework, so it is to your benefit to attend recitations.


