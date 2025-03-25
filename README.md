# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.


//


Name: Kane Kriz

Start Date: 11 Feb 2025
Last Edited: 24 March 2025
Feedback Request 1 Date: X


//


Response: Not Complete
Directly from slide 34, a good pivot is considered the center n/2 pivots, between n/4 and 3n/4
Choosing any element randomly (most efficient to thus simply choose the first element in the array) results in a likelihood of 1/2 for the first random element to fall under a "good pivot".
This is due to n/2 taking up one half of the elements, giving the randomly selected first element a 1/2 chance of being within the "good" n/2 center between n/4 and 3n/4.
This is covered within the slides.

Now we must move towards figuring out the probability of selecting a "good" pivot, but now via the method of inspecting the first, middle, and last elements of an array, then choosing the median value of them.
We must still consider that as the array is randomly sorted, each of these chosen elements (Index 0, middle positon via length of array / 2 rounded if needed, and final position at index arrayLength -1) has an equal chance to be anywhere within the array numerically.


Mathmatically, this can be seen via considering the possible outcomes of each of the three selected values being within or otuside of the desired n/2 center range.
Take, for instance, if all three (position 0, middle position, end position) are all outside of the desired "good" pivot range. Then the selected pivot from the median would be forced to be out of the good range.

So the permutations would be: 
GGG

GGB GBG BGG 

BBG GBB BGB

BBB

With "G" signifying that a value is within the "good" center range for pivots, and "B" meaning a bad pivot outside of the center range.
All permutations sharing a row above are in essence the same, as the median pivot selector is assumed to sort the three values taken from the three outlined positions, as they are from a presumably unsorted list and thus have an equal likelihood to be any value.

The easiest to consider are the GGG and BBB, corresponding to all three selected indexes holding values that are either all within or outside of the desired range, respectively.

Next, we can consider



//



Plagiarism Acknowledgement: I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

Citations:
Slide 34 of the Sorting Lecture in-class slides.

And the provided gitHub documentation already pasted earlier within this md file.
