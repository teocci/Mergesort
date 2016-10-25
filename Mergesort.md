Interview Questions (optional)

1. Merging with smaller auxiliary array. Suppose that the sub-array a[0] to a[n−1] is sorted and the sub-array a[n] to a[2∗n−1] is sorted. How can you merge the two sub-arrays so that a[0] to a[2∗n−1] is sorted using an auxiliary array of length n (instead of 2n)?

Step 1. Copy the left sub-array {a[0], a[1], .., a[n-1]} into the auxiliary array {aux[0], aux[1], .., aux[n-1]}. 
Step 2. Set a counter i = 0 at the first element of the auxiliary array: aux[0], j = 0 at the first element of the right sub-array: a[n] and k = 0 at the first element of the left sub-array: a[0].
Step 3. Repeat until all the elements in the auxiliary array and the sub-array {a[n], a[n+1], .., a[2n-1]} are placed in the array.
	Step 3A. Compare the auxiliary array aux[i] and the right sub-array a[j].
	Step 3B. If a[j] > aux[i] then a[k] = a[j] and k++, j++;
	Step 3C. Else, if a[k] = aux[i] then a[k] = a[i] and k++, i++; 



2. Counting inversions. An inversion in an array a[] is a pair of entries a[i] and a[j] such that i<j but a[i]>a[j]. Given an array, design a linearithmic algorithm to count the number of inversions.

Step 1. We have a merge-sorted array a[] and we create an auxiliary array aux[].
Step 2. Repeat until there are no more elements in a[]. Take a[1] and find its position in sorted array aux[] via a binary search. The number of inversions for this element will be one less than the index number of its position in aux[] since every lower number that appears after the first element of a[] will be an inversion.
	Step 2A. Accumulate the number of inversions to counter variable (inversions).
	Step 2B. Remove a[1] from array a[] and also from its corresponding position in array aux[]

Step 1 (merge sort) would take O(n * log n) to execute. 
Step 2 would execute n times and at each execution would perform a binary search that takes O(log n) to run for a total of O(n * log n). 
The total running time would be O(n * log n) + O(n * log n) = O(n * log n).




What do you think?

3. Shuffling a linked list. Given a singly-linked list containing n items, rearrange the items uniformly at random. Your algorithm should consume a logarithmic (or constant) amount of extra memory and run in time proportional to n*logn in the worst case.

 
We need to design a linear-time subroutine that can take two uniformly shuffled linked lists of sizes l1 and l2 and combined them into a uniformly shuffled linked lists of size l1 + l2. To this end:
Step 1. Split the linked list into two
Step 2. Create a pointer array pointing at each node.
Step 3. Shuffle each list.
Step 4. Make the two list have the same length, if not append a dummy node for the shorter one with value -1;.
Step 5. Iterate the array from 0 to n, swapping the current item with a random item after current. generate a random number r between [i, n) swap a[i] with a[r].
	Step 5A. While traveling through the linked list merge the two sub-list randomly. 
	Step 5B. Select from the two lists by generating a random number r between [i, N) swap a[i] with a[r].



### how to sum big o
* [How would you explain O(log n) in algorithms to 1st year undergrad student?](https://www.quora.com/How-would-you-explain-O-log-n-in-algorithms-to-1st-year-undergrad-student)
* [Sum of big O notation [duplicate]](http://stackoverflow.com/questions/12946600)
* [Big O when adding together different routines](http://stackoverflow.com/questions/7007723)
* [Merging two sorted arrays with smaller auxiliary array ](http://www.algoqueue.com/algoqueue/default/view/983040/merging-two-sorted-arrays-with-smaller-auxiliary-array)
* [Programming Assignment 3 Checklist Pattern Recognition](https://github.com/i026e/Algs4_Projects/blob/master/3_Collinear_Points/Programming%20Assignment%203%20Checklist%20%20Pattern%20Recognition.html)
* [Week 3 - Pattern Recognition](https://github.com/ISchwarz23/Algorithms-Part1---Assignments/blob/master/Week%203%20-%20Pattern%20Recognition/src/SampleClient.java)
* [The For-Each Loop](http://docs.oracle.com/javase/1.5.0/docs/guide/language/foreach.html)
* [How to Randomly Shuffle a Linked List in C](http://stackoverflow.com/questions/11309200)
* [Algorithm for Shuffling a Linked List in n log n time](http://stackoverflow.com/questions/12167630)
* [ArrayIndexOutOfBoundsException when shuffling a LinkedList](http://stackoverflow.com/questions/26125963)
* [Knowledge](https://github.com/guibin/Knowledge/tree/master/libs/lib.algorithm/src/main/java/guibin/zhang/leetcode/listAndArray)
* [Solutions](https://www.coursehero.com/file/p577o78/You-will-be-able-to-view-your-score-after-the-deadline-passes-These-interview/)
* [Counting inversions in an array](http://stackoverflow.com/questions/337664)
* [Merging two sorted arrays with smaller auxiliary array ](http://www.algoqueue.com/algoqueue/default/view/983040/merging-two-sorted-arrays-with-smaller-auxiliary-array)
* [MergeWithSmallAux.java](https://github.com/guibin/Knowledge/blob/master/libs/lib.algorithm/src/main/java/guibin/zhang/onlinecourse/MergeWithSmallAux.java)
* [algorithms-part1](https://github.com/eschwabe/interview-practice/tree/master/coursera/algorithms-part1)
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()
* []()