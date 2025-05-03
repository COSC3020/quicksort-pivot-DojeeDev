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

### Analysis

Instead of looking at the probability of median of three working, lets look at the probability of it not working. 

When more than one of H (high values) or more than one of L (low values) are chosen, even if one of the values is M (mid, aka the one we want), the median value will not be M (if there exists an M in the choice of 3, if there is no M in the choice of 3, the value picked can't be M anyway.)

For L and H there are 3 ways for there to be two of them. For two Ls and one M. LLM, LML, MLL. Same applies for H. Therefore we multiply the probablity of two Ls by 3

Therefore the odds of picking a bad pivot using this method denoted B is 

$B = 3\cdot (\frac{1}{4})^2 + 3 \cdot (\frac{1}{4})^2 = 3\cdot(\frac{1}{16} + \frac{1}{16}) = 3\cdot\frac{1}{8}$.   Meaning that the odds that the pivot is good is: $G = 1 - \frac{3}{8} = \frac{5}{8} > \frac{1}{2}$ So median of 3 is better than picking at random.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

