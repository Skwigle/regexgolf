This one is probably my favorite lesson I've done so far. Not because of what you need to know, but because of the pattern itself. With this lesson, the first thing you need to do is look very carefully to try and understand what the pattern is. This one is pretty different. (Hint: The name is a pretty big hint.)

Give up? If you look at the right column, you'll see that all the words have a palindrome within them. For instance, the word "bassarisk" contains "assa", the word "engrammatic" contains "amma", etc. Well, that's great and all, but we need to be matching the words on the left, not the right. So I guess it's time to look up how to match things that are NOT your regular expression.

I had a nightmare of a time looking this up. If you can't find it, don't feel discouraged. What you're looking for is "(?! )"(The white space is where your code would go.) What this syntax is saying is essentially "Everything but the code in the parenthesis." Now we need to find a way to use it! Give it a shot yourself. If you want a little direction, I started with trying to match the palindrome itself, and from there figured out how to match everything but. Good luck!

Hopefully you hit it out the park! If not, I'm here to help. For starters, let's try to get the palindrome. The easiest way to do this is going to be by using backreferences. The code we are looking for is: "(.)(.)/2/1" (No quotes, as always). Now that we got that, we need to find a way to match everything but that palindrome. For starters, we know that most of the words in the right column have letters before the palindrome. So that changes the expression to ".*(.)(.)\2\1". 

It seems as if we could just throw that code into the syntax ( "(?!.*(.)(.)\2\1)" ), but when we try that you'll see that every word matches. Why is that? It's because Regular Expressions are a little unruly. This code has too much freedom, so it is starting wherever it has to to make the code work. In this instance, it is starting right after the first letter of each palindrome. For example: In the word "overattached", it is starting at "ttached", and there's no palindrome in that, so it works.

So how do we fix this? Simple. Anchors! Well.....Anchor. All you need to do is tell the code where to start. Adding a simple Anchor(^) will solve all our issues! This changes the code to "^(?!.*(.)(.)\2\1)" and we're done!

For the code breakdown, I will try to keep it simple since we went pretty in depth while creating it:
```
^                            (?!                                  .*                                  
Starting from the beginning: Match everything except strings with zero or more characters followed by a

(.)                      (.)                             \2                                         
specific character and another specific character, then repeats the second specific character followed by

\1                          )
the first specific character.
```
Pretty simple once it's broken down.

Answer: ^(?!.*(.)(.)\2\1)
