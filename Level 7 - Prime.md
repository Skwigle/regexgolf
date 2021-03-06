This is where Regex Golf starts getting very tricky. Right off the bat, you can probably guess the pattern based on the title.
We are trying to make a regular expression to look for prime numbers. It sounds like you can do it pretty simply, but it is actually much easier to come up with code to not include numbers that aren't prime.

Try to make some code that will only find prime numbers.

After a lot of messing around, trying to wrap my head around this level, I eventually came up with: "^(?!(xx+)\1+$)". I have absolutely no idea if this can be shorter, so if yours is, congrats!

I will admit, I found the code before I understood it. Even while knowing the code and what it is saying, it is still a little confusing, but I will do my best to explain it.

What the code is saying is:
```
^     - Begins
(?!   - Do not match any of the strings that match what else is in these parentheses
(xx+) - There will be two or x's (Or won't be due to "(?!")
\1+   - However many x's were previously used are used again one or more times
$)    - Code ends
```

After messing around with the anchor, I think I now grasp why the anchor($) has to be in the parentheses. If you take the  anchor out entirely, then you're giving your code too much freedom and it will just go wacky, matching anything with four or more x's.

That wont work. I then tried putting the anchor outside the parentheses, and that matched absolutely nothing. It left me  scratching my head. I believe the reason why, is that once you do that, you're telling your code "Don't match this stuff" but other than that, it's trying to match "^$", which would be nothing. So that also doesn't work. So you place the anchor where it needs to be to tell your workaround code to close. So in the end, all you're doing is giving it what to not match, but leaving the end open so you can match literally everything but what the code matches. Confusing stuff, I know, but it just gets harder from here.

Answer: ^(?!(xx+)\1+$)
