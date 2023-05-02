Download Link: https://assignmentchef.com/product/solved-comp1020-lab8-arraylists
<br>
<ul>

 <li>ArrayLists</li>

</ul>

Notes:

<ul>

 <li>The three exercises are independent – they can be done in any order.</li>

 <li>Only one of the three exercises is required.</li>

 <li>Try to complete as many as you can.</li>

</ul>




Most of the basic <strong>ArrayList</strong> operations: <strong>size</strong>, <strong>add</strong>, <strong>remove</strong>, <strong>get</strong>, and <strong>indexOf</strong>, are used in this problem. Generic <strong>ArrayLists</strong> (not <strong>ArrayList&lt;</strong><strong>Type</strong><strong>&gt;</strong>) will be used in all of the exercises in this lab.

Begin with the file <strong>TemplateLab8Bronze.java</strong>. Complete the method

<strong>ArrayList extractDuplicates(ArrayList a1, ArrayList a2)</strong>

which will look for elements that appear in <em>both</em> <strong><sub>a1</sub></strong> and <strong><sub>a2</sub></strong>. When one is found, it should be removed from <em>both</em> <strong><sub>a1</sub></strong> and <strong><sub>a2</sub></strong>. You can assume that neither list will contain a value more than once. An <strong>ArrayList</strong> containing all of the elements that were <em>removed</em> should be returned as the result of the method.

The output printed by the main method should be:

<strong>a1 is [45, 12, 98, 34, 6, 42] a2 is [6, 81, 36, 12, 77, 42] removed elements: [42, 6, 12] a1 is now [45, 98, 34] a2 is now [81, 36, 77] </strong>Notes:

<ol>

 <li>When you’re going through all of the elements of a list, but you’re shrinking the list at the same time, unexpected things may happen. Write the loop very carefully. You can’t just use the usual <strong>for</strong></li>

 <li>If you use <strong>get( )</strong> to obtain an element from <strong>a1</strong> or <strong>a2</strong>, its type will be <strong>Object</strong>.</li>

</ol>




<ol>

 <li>An <strong>ArrayList</strong> is a good way to store a deck of cards (or a partial deck, or a hand). Begin with the file <strong>java</strong> and then complete the three small methods whose headers appear at the bottom of the file.</li>

</ol>




<ol start="2">

 <li>Complete the method <strong>ArrayList makeDeck(int numCards)</strong> which should return a new <strong>ArrayList</strong> containing the numbers from <strong>0</strong> to <strong>numCards-1</strong>. (These numbers will have type</li>

</ol>

<strong>Integer</strong>, not <strong>int</strong>, but since the two are interchangeable it will make no real difference.)

<ol start="3">

 <li>Complete the method <strong>void shuffle(ArrayList deck)</strong> which will rearrange the elements of <strong>deck</strong> into a random order. The usual technique is: Choose a random card position from <strong><sub>0</sub></strong> to <strong>size()-1</strong>. Delete the card in that position and put it in position <strong>0</strong> instead. From now on, leave that card alone. Choose a random card position from <strong>1</strong> to <strong>deck.size()-1</strong>. Delete the card in that position. Put it in position <strong>1</strong>. And so on for positions <strong>2..deck.size()-2</strong>. (There’s no need to select a random card to go into position <strong>deck.size()-1</strong> because there’s only one card left at that point anyway.)</li>

 <li>Complete the method <strong>ArrayList[] deal(ArrayList deck, int numHands, int numCards)</strong> which will deal the indicated number of hands, with the indicated number of cards in each hand, from the top of the deck. The cards that are dealt should be <em>removed</em> from the deck. It should return an array of <strong>ArrayList</strong>s, where each <strong>ArrayList</strong> contains the cards in one hand. It should deal in the normal way, with consecutive cards going into different hands, in a circular manner, as shown in the example below.</li>

 <li>When the main method is run, it should produce random output similar to the following. A small deck of only 20 cards is used to keep the output small.</li>

</ol>

<strong>The new deck is [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19] </strong>

<strong>The shuffled deck is [11, 14, 19, 2, 17, 1, 7, 9, 6, 8, 10, 3, 12, 16, 4, 15, 13, 5, 0, 18] </strong>

<strong>How many hands should be dealt? 3 How many cards in each hand? 4 </strong>

<strong>The hands are: </strong>

<strong>Hand 0: [11, 2, 7, 8] </strong>

<strong>Hand 1: [14, 17, 9, 10] </strong>

<strong>Hand 2: [19, 1, 6, 3] </strong>

<strong>The remaining deck: [12, 16, 4, 15, 13, 5, 0, 18]</strong>




The elements in an <strong>ArrayList</strong> may be any type of <strong>Object</strong>, including other <strong>ArrayLists</strong>. Such “nested lists” are very powerful and flexible, and in fact there are entire languages built around this idea.

<ol>

 <li>Begin with the file <strong>java</strong>. Take a look at the <strong>main</strong> method, and run the program and look at the output. This program creates <strong>ArrayLists</strong> nested inside other <strong>ArrayLists</strong>, to a depth of 4 levels.</li>

 <li>Complete the method <strong>ArrayList flatten(ArrayList a)</strong> at the bottom of the file. This method should accept an <strong>ArrayList a</strong>, which may contain other <strong>ArrayLists</strong> inside it, nested to any depth. It should create and return a new <strong>ArrayList</strong> which is a “flattened” version of the original, which still contains all the data that was present in the original, in the same order, but with the nesting removed (essentially, the <strong><sub>[]</sub></strong> should disappear). See the sample output below.</li>

 <li>The correct output from the main method, once <strong>flatten</strong> is working, is:</li>

</ol>

<strong>The nested ArrayList is: [23, [19, 46], Hello, [45.5, World, [11, 22, [33]]]] The flattened ArrayList is: [23, 19, 46, Hello, 45.5, World, 11, 22, 33] </strong>

<ol start="4">

 <li>Note: If <strong>a1</strong> and <strong>a2</strong> are both <strong>ArrayList</strong> objects, then <strong>addAll(a2)</strong> will add all of the elements of <strong><sub>a2</sub></strong> to the end of <strong><sub>a1</sub></strong> (a concatenation operation like + for Strings). That would be useful here.</li>

</ol>