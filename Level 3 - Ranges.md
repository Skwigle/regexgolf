Being new to Regular Expressions, this level threw me a curveball. The first thing we need to do, as always, is scope out the pattern. If you look at the column on the left, you can see that all the words only use the letters A through F. This is where the name "Ranges" comes from. Look up Ranges and see if you can solve it yourself.

There are two very similar answers you might've gotten, and I will cover both to make sure you understand both of them. A lot of times with Regular Expressions, especially when starting out, it can be more confusing why something didn't work than why the correct solution did. If you're like me, you probably tried ^[a-f]$ and afterwards decided to check your wall to judge the amount of brain damage you'd cause by slamming your head into it.

Before I explain why that doesn't work, I will explain the new symbol we are using: ^. This symbol is very similar to the dollar sign we used in the last lesson. The difference is ^ is used for "beginning with" while $ is used for "ending with". The trick here is that when using both symbols, you are claiming "everything between will describe the word or string from beginning to end." So when writing ^[a-f]$, you are saying "find a word where, from beginning to end, it is one letter, A through F." The words we are looking for are more than one letter long, and that is why this doesn't work. What we need is a "Quantifier".

A quantifier is a command you can use to claim something occurs "More than once", "Two to Four times", pretty much any amount of times you need it to. This is where the multiple answers come into play. The main two answers to go for (for minimal character usage) are "^[a-f]+$" and "^[a-f]*$" (without quotation marks). Although both work, they do not necessarily look for the same things.

^[a-f]+$ - When you break this one down, it is saying "Find me a word or string that has the letter A through F 'one or more times' and ONLY has those letters." The + symbol is a quantifier that says [a-f] will happen one or more times.

^[a-f]*$ - This one is pretty similar. The difference in this command is the quantifier. While the + symbol said [a-f] will be happening 'one or more times', the * symbol claims that [a-f] will be happening 'zero or more times'. This may be confusing now, but we will definitely be using and touching up on this command later.

Answer: ^[a-f]*$ or ^[a-f]+$
