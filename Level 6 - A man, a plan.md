This one is a fun one. Once again, the title to this level is a pretty large giveaway as to what the pattern is. The title is a part of a well known palindrome "A man a plan a canal panama". So right off the bat, we now know the pattern probably has to do with palindromes.

So for this level, I will not only be showing you the initial answer I got, but I will also be showing you a secondary (shorter) answer I came across at a later time.

If you look at the left column, you'll see that we're actually trying to match palindromes this time. More importantly  though, the entire word this time is a palindrome as apposed to before when it was purely a portion of it. More importantly, this is the level to test your true grasp on what we've covered so far! There is absolutely nothing new you need to learn to solve this level. (There are new things we will be learning, but I will cover that afterwards.)

Any luck solving it? The simplest answer I was able to come up with (not shortest, simplest) is: ^(.)(.).*\2\1$ 
What this is saying is "From beginning to end, there will be a character(1), followed by another character(2), then there may (or may not) be some characters, character(2) is used again, and the word will end with character(1)"

Now we move on to the way you could have solved it in a shorter fashion. This way also requires you learning something new. To start off, see if you can find a way to search for a character that is not a specific character. If you don't know which letter you're not including, just try to pay close attention to what our last code was matching. Not sure of a bigger hint I can provide without giving it away directly.

So the problematic word here is "sporous", and that is because it is the only word in the right column that both starts and ends with the same letter. If it weren't for that word, we could very easily just write "^(.).*\1$" and call it a day. Unfortunately, it isn't that simple. We need to find a way to specify "not this specific character". Conveniently, "sporous" has a letter that isn't present in any of the words in the left column. Take a look and see which letter it is.

Shouldn't have been too hard to spot. So, if you couldn't find the way to say "not this character", you were looking for "[^x]" (Where 'x' is the letter you're saying it can't be). The letter that we are not allowing to participate in our search is "p". It's the only letter that appears nowhere in the left column. More importantly, we need to place the new thing we learned in the proper place. The only way that could work is: ^(.)[^p].*\1$

Now, this code's explanation is very similar to the earlier one, but since there are some new differences, let's go over the new code. So it is saying "From beginning to end, there will be any character(1), followed by a character that is not 'p', then zero or more characters after that, then character(1) once again at the end."

Answer: ^(.)[^p].*\1$
