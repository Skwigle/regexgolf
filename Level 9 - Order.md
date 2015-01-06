I feel the need to tell you: This level's answer will be starting a little ridiculous, but it gets tame by the end, so make sure to stay with me here! Try to find the pattern! Once again, the pattern is a little more subtle this time. Now, I feel there is a term here I need to clarify: Cheat. They are not saying "Look up the answer and move on." The term "Cheat" in this sense is saying "make an expression that specifically works in this situation, but you will (more than likely) never actually use in the real world ever."

So, if you haven't found the pattern, it's pretty simple once you know it. If you take a look at all the words in the left column, you can see that all the words have all their letters in alphabetical order. That's it! We have to find a way to find words in alphabetical order. Give that a shot, see what you come up with.

Now, the embarassing part. This is what I came up with initially: ^a\*b\*c\*d\*e\*f\*g\*h\*i\*j\*k\*l\*m\*n\*o\*p\*q\*r\*s\*t\*u\*v\*w\*x\*y\*z*$

Is it pretty? No. Is it worth a lot of points? No, but it will work with any words that have all their letters in alphabetical order. So this works, but it is excessively long. Also, there was that term "Cheat" they used earlier. This could actually be used later on. That's not cheating. Let's cheat! Try to find a way to shrink it up.

Before I say the answer I got, I will let you know: I'm almost positive there is a smaller way to do this. So if you found a smaller way to write this out: Congrats!

The answer I came up with was ^[a-m].{1,5}$

It took me a little while to come up with that code, but it is MUCH smaller than the previous code we had. There isn't really anything new in this answer, so I'll keep the breakdown fairly simple.

What this code is saying is "From beginning to end, there will be a character between the range of 'a' and 'm', followed by 1 to 5 of any character, then it ends."

One thing I want to clarify: after making the code, I noticed that there was no need for making it one to five characters. You can very simply make it 4 or 5 as that works as well, and is probably even closer to cheating. So we will go with that!

Answer: ^[a-m].{4,5}$
