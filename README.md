# Algorithm-check_point


Steps

The idea is lets say we have two arrays namely set1= [1, 3, 5 ] and set2= [2, 6, 5]

In the example above the distinct elements are [1, 3, 2, 6]. Distinct element is one that is not common to both steps
sum= 1+3+2+6 =12

So how do we compare both arrays programmatically?

Its simple to do this. We have to compare each element of both arrays with each other.

So i would that the first element in set1 which is [1] for instance and compare it set2 [2,6,5] then i would do this for the next element in set1 which is [3] and then the same for the next element which is [5]. This way we can get distinct elements in set1 which is [1, 3]

The next step is to take each element of set2 and compare it with set1 array. So we take the first element which is [2] and compare it with set1[1,3,5], then the next element which is [6] and compare it with [1,3,5] set 1 again and then the last element of set2 which is [5]. This way we can get the distinct elements in set2 which is [2, 6]


To make this task simple we would make use of functions to braeak the algorithm

First we create a function that compares an element with every element in another array. In this case I named it is_distinct_element. It has two parameters one is an element and the other is the other array we are comparing the element with. Try to relate this with the instances in paragraph 12 and 14 above

This function has a for loop which iterates throught the other array (line 4 in sets.algo). In other words it is trying to find a number if it exists in that other array. 
If the number exists let the function *return false* else let it *return true* (sets.algo line 5-9)

Now for the algorithm itself name sum_up_distinct_elements

Next we declare our variables :
Initialize sum to zero
Declare set1 array which has a length of s1 
Declare set2 array which has a length of s2
(Recall that length of ann array is the number of elements in the array)
Initialize j,k to zero which are counts for both times we do an iteration in the algorithm.

Recall: 
First algorithm loop is to compare each element of the first array (set1) with the other array in this case the second array (set2)
Second algorithm loop is to compare each element of the second array (set2) with the other array in this case the first array (set1)

1st loop ex (ref: Line 26 to 30)
set1= [1, 3, 5 ] and set2=[2, 6, 5]

It will loop from j= 0 to s1-1 which mean j would have values from 0 to 3-1=2  (step 1 means increment by 1 after each time)
first loop will run for j=0, j=1 and j=2


for j=0, it would compare set1[j] and set2 which is set1[0] is 1 and the other array to be compared with is set2 which is [2,6,5]

for j=1 .... set1[1] and set2
for j=2 .... set1[2] and set2

Now lets recall that is_distinct_element returns true if after comparism it doesnt find the element (set1[j]) in set2 as is the case for the firt loop example (reference to sets.algo line 26- line 30)
so we used an if statement for that compare so that the value of sum which was initially zero is only updated if after comparism the function returns true

second loop ex (ref: Line 32 to 36)
set1= [1, 3, 5 ] and set2=[2, 6, 5]

It will loop from k= 0 to s2-1 which means k would have values from 0 to 3-1=2  (step 1 means increment by 1 after each time)
second loop will run for k=0, k=1 and k=2


for k=0, it would compare set2[k] and set1 which is set2[0] is 2 and the other array to be compared with is set2 which is [1,3,5]

for k=1 .... set2[1] and set1
for k=2 .... set2[2] and set1

Now lets recall again that is_distinct_element returns true if after comparism it doesnt find the element (set2[k]) in set1 as is the case for the second loop example (reference to sets.algo line 32- line 36)
so we used an if statement for that compare so that the value of sum which was initially zero is only updated if after comparism the function returns true

At the end of both loops sum would have an updated value of the addition of uncommon/ distinct elements in both arrays
