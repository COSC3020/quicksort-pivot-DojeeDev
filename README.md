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

Let L be the odds of picking a Low (1/4), M for mid aka good (1/2), and H for high (1/4). $B_L$ for Bad pivot combo with 2 or more lows and $B_H$ for bad pivot combo with two or more highs.

$B_L = LLL+LLH+LHL+HHL+LLM+LML+MML = \frac{5}{32}$

$B_H = HHH+HHL+HLH+LHH+HHM+HMH+MHH = \frac{5}{32}$

$B = B_L + B_H = \frac{5}{32} + \frac{5}{32} = \frac{10}{32} = \frac{5}{16}$

Probablity of good pivot = $1 - \frac{5}{16} = \frac{11}{16}$

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

