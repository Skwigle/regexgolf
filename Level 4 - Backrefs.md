Backreferences can be horrendously tricky if you don't know what you're looking at. Try to look them up if you can. If you get stumped, I will explain them here for you.

Let's say we're trying to find the word "banana". We can do that with backreferences by typing:
.(.).\1.\1
or you could also do it by typing:
(.)(.).\2.\2

That second example might confuse you, but I put it in there just to give you a thorough explanation. Do not get frustrated, this will be explained!

When you look at the first example, you can see a new element (\1). This is a backreference. What it is claiming is "use whatever that first parentheses was". So in the sake of the word "banana", the first period was "b", then we put "a" in parentheses since we'd be using it again. So when we hit the \1, it's calling back to the parentheses that will contain the first "a" in "banana" and reusing it. Still a little confusing? We'll try to break it down further:

. (.) .  \1 .  \1
b  a  n  a  n  a
         ^     ^
    It's as if both of these are reusing the previous "a" in the parentheses back there.

Now for the second example. If you notice, this example is using "\2" instead of "\1". The reason why is that this example is calling out to the second parentheses. If you look at the example, you will see that I put the first period in parentheses. If I called for "\1" it would assume I was looking for the letter "b". Now that you know about how numbers work in backrefernces, you could even write it out like this:
.(.)(.)\1\2\1
Since you are reusing the letter "a" as well as "n", this will work just fine.

Are you tired of learning about backreferences? Well too bad! We still have a level to solve! Take a look at the words and try to find a pattern! Did you find it? Either way, I'll explain it.

So take a look at the left column. Theres something interesting about the first couple letters. If you haven't gotten it yet, the first three letters appear later on in the word. So now that we understand how backreferences work, we can come up with something to find those words.

So, the answer we're looking for is : "(...).*\1". (no quotes)

You might have written "^(...).*\1", and that works, but this is Regexgolf, so we're looking for the least amount of characters. So what this expression is claiming is "There are 3 letters, then possibly some random letters after that, but eventually those 3 letters appear again in the exact same order". You might also notice that we left the end open. The reason we dont use anchors in this level is due to words like "anticovenanting". We only need our search to reach "anticovenant". You can continue it if you want, and write it out as "^(...).*\1.*$". That does work, but Regexgolf and all that. Figure you're tired of me stating the obvious...

Answer: (...).*\1
