---
layout: post
title:  "Affirmations at the Command Line"
subtitle: "Creating a CLI for Goals"
date:   2016-06-09
bigimg: /img/affirmations-cli.png
---

Scott Adams has discussed the use of affirmations in his books [_The Dilbert Future_](http://amzn.to/1UEIs5m) and [_God's Debris_](http://amzn.to/1U9qtH7), and most recently on [The Tim Ferriss Show podcast](http://fourhourworkweek.com/2015/09/22/scott-adams-the-man-behind-dilbert/). (And a bunch of other places as well.)

 > The idea behind affirmations is that you simply write down your goals 15 times a day and somehow, as if by magic, coincidences start to build until you achieve your objective against all odds.  
 > An affirmation is a simple sentence such as “I Scott Adams will become a syndicated cartoonist.” (That’s one I actually used.)

I have recently begun the practice of affirmations, in service to my current [goal of making $250 a day](http://250aday.github.io/2016-05-31-intro-goal/). I don't have any reason to believe that affirmations actually work (or even that [my goal is even achievable within the aloted timeframe](http://250aday.github.io/2016-06-01-good-goal/)). But my general impression of Scott Adams is that he is way richer than I am, so his advice carries some weight. Since the cost of following this routine is extremely low (less than 5 minutes a day), it seems worth experimenting.

Until recently, I have been writing my affirmation in my [favorite notebook](http://amzn.to/1rflAlr), but that hurts my hand and my writing becomes completely illegible. I had thought about typing my affirmations, but something about that struck me as missing out on the "magic" of the thing.

But in his interview with Ferriss, Adams says that he is "sure" that typing it would produce the same effect (whatever that effect might be). So, I've typed it a few times. But that seemed unsatisfying as well. Do I delete the file afterward? Do I save it? Do I have a single file and add 15 lines to it everyday? And I'm still struck by the fact that typing something into a file doesn't feel like doing something quite the same way writing does.

But you know what __does__ feel like accomplishing something? Typing at the command line.

![Terminal Window](/img/terminal-window.png)

So, if the whole thing is a trick of psychology (and I strongly believe that it is), why not _trick my mind_ by making myself believe that I was issuing commands. These commands could be directed toward "the Universe" or to "my subconscious" or whatever.

So that's what I did. I wrote a little [Python script for writing affirmations at the command line](https://gist.github.com/adammichaelwood/c58fa55350cce2f46ad0027f4c4e2097).

<script src="https://gist.github.com/adammichaelwood/c58fa55350cce2f46ad0027f4c4e2097.js"></script>

Here's how it works:

 - Start the program.
 - It prompts for your name.
 - It prompts for your affirmation.
 - It repeats back to you, in second person, your affirmation ("You will..."). It displays this feedback a random number of times, in different colors, with a tiny, random pause between each repetition.
 - It again prompts for your affirmation and repeats it back to you.
 - Once you have entered and received back your affirmation enough times (random, around 15), it tells you that "you have proved yourself worthy" and exits.

I worked on this a little too long, iterating from a very simple counted loop to this silly thing I have now with a lot of randomness and colors and Monty Python jokes. I like to think all of these "tweaks" were meaningful, so let me explain why I think so...

### Jokes

The prompts and final affirmation are quotes from [Monty Python and the Holy Grail](http://amzn.to/1UENHSu). Even a slight hint of this movie makes me laugh (or at least smile) a little bit. It also reminds me of a time when I was really into Monty Python: my youth, which (as for most of us) was a very hopeful time, when I thought anything was possible. Recapturing even a whiff of that seems good. And humor is disarming, which is helpful for any kind of persuasion.

### Randomness

I set points of randomness in the script: the number of affirmations required by the user, the number of times the affirmation would be repeated back, the amount of time between each repetition of feedback, and the colors.

The randomness creates an unexpected experience. The part I need drilled into me (the affirmation itself) doesn't change, but little things about the way I experience it change. From my understanding of [_Impossible to Ignore: Creating Memorable Content to Influence Decisions_](http://amzn.to/1PMTfi0), by Carmen Simon, this novelty will help me remember and persuade myself to take action.

(BTW - That could be a terrible reading of that book. I'm only about 1/4 of the way through it at the moment.)

Additionally, the randomness provides a (completely fictional, I'm sure) sense of somehow inviting luck. I can let the superstitious part of my brain think, "I have typed this and read this exactly the number of times I needed." This is a fantasy, of course, but a helpful one. Additionally, it reminds me to _cooperate with probabilities_, which is one way to [generate your own luck](http://lifehacker.com/how-to-create-your-own-luck-1693949106).

### Time delay

In my mind, the most important tweak I made was the tiny, random time delay between each affirmation feedback. This accomplishes three things, and only one is woo-woo-weird.

First of all, it makes me read the feedback. I can't not read words that are in front of me (I know, I've tried), so even though I already know what it is going to say, I read it anyway. Again and again and again.

Secondly, along with that, it gives me time to reflect on the affirmation. It's like a micro-meditation.

Finally --- and this is crazy --- it provides me the illusion that the computer is _working on the problem_.

Computers are magic boxes that **only do what you tell them to do**. My rational mind knows that the time delay is caused by the `time.sleep()` function and that the delay will be some randomized fraction of a second, and that nothing is happening. But my irrational mind thinks, "I just commanded my magic light box to make me rich, and now it is working on that problem."

### Bonus: The best import statements, ever

I had to import three modules to do all the added silly things. Scroll back up and look at them.

In my original, non-random, non-colored, non-delayed version, I didn't need them. After I finished I realized I couldn't have asked for a better set of module names to import. 

## Will all this work?

![Elliphino](/img/elliphino.jpg)

I think so. At least as much as affirmations in general, and maybe more beyond that. Also, it gave me some practice with Python, and something to blog about. Which means that _even if it does nothing at all and affirmations don't work_, it was still not wasted time. And the risk is extremely low.

That seems like cooperating with probabilities to me.
