So now we know precisely what they're looking for. So let's move on to the next lesson. Like we did with the last lesson, the first step here will be looking for the pattern. Once again, the pattern here is pretty apparent. If you look at all the words in the left column, you see that every one of those words ends in "ick". So we need to find a way to look for "ends in 'ick'". 

Now, you might be reading this and thinking "it can get smaller than that..." Good! You caught it! If not, I will continue the way I initially did the level.

With a lot of these levels, the name of the level will give you a hint of what to look for. This level is called "Anchors", so, look up what Regex Anchors is! (Looking things up, and figuring them out on your own will always be the best way to learn. It can be hard, but it truly is the best way.)

Once you have read up on Anchors, the answer is pretty obvious. "ick$". Let's break down and see what this is saying:

The anchor is claiming "ends with". The 'ick' portion is purely claiming what it ends with. So this simply states to look for "words that end in 'ick'" Now, this is Regex Golf, so we're looking for the shortest answer. So, let's shrink it up! So, for starters: we can see that all the words in the left column all end in "ck", so let's try "ck$". Look, it works! But we can still try to shrink it further. All the words end in "k", so let's try "k$". That works too! Now...we have only 2 characters. Words in the right do have the letter K in them, so we need the anchor in place. So that means we're done! With the highest score nontheless! Time to move on!

Answer: "k$"
