I know some of us are still recovering from Level 7, but the show must go on! If it helps any, this level is nowhere near as 
confusing as the last. Time to find the pattern! The hint in the title is a little more subtle this time.

Find it? If not, the pattern is that each word in the left column has a vowel that repeats four times in each word. 
Unfortunately, it isn't the same vowel. That'd be too easy. So we need to make this work for different vowels. Figure out how
to do that! GO!

Alright, if you've moved on, you either figured it out or gave up. Now, earlier I brought up that you might have crazy long 
code, then shorten it up once you have code that works. I will go through my entire process of code I had that worked, so you
can get an idea of what I mean. So, my starting code was: ^.*([aeio]).*\1.*\1.*\1

The code works, so that's good. It's also flooded with unnecessary stuff. I started off thinking "Well...it doesn't really
matter how it starts, right?" So I deleted the beginning and was left with: ([aeio]).*\1.*\1.*\1

Code still worked, but it can probably get shorter. So I looked, and thought to myself "Each vowel is actually only divided by
one other character..." So, we delete the asterisks and we're left with: ([aeio]).\1.\1.\1

That's about as good as it's going to get, right? Wrong. This is Regex Golf, I need all the points I can get. This is only worth
193 points, I know I can at least get a couple more. So I notice there's a little repetition going on, so we can shorten that u
, and after doing so, we're left with: ([aeio])(.\1){3}

There we go! Squeezed one last point out of it. I feel the need to point out. I'm sure there is a shorter way to do this, but I
am happy with 194, so I'll leave the shorter answer for you to figure out! (I know, it's hard to handle my generousity.) On to
Level 9!

Answer: ([aeio])(.\1){3}
