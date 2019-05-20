---
layout: post
title:  An introduction to the math of Magic the Gathering card draw
---

Magic has a rich set of mechanics, but it all revolves around drawing cards. Card games are well studied in mathematics and these ideas can be applied to Magic the Gathering as well. Anyone who's taken a course in probability or combinatorics know card games and dice are a favourite among text book authors. 

In this short series we will look at a couple of different questions, you as a player, may have when building a deck for Magic.

I'm most familiar with 40 card, limited, decks, and we will base our scenarios on this. But usually you can just substitute 40 for 60 and the question, and its answer will hold.

## Who's this for?
Obviously you like Magic, or have an interest. Maybe you want to answer some of the common questions you have when you are building a Magic deck without entering it into a computer. Or maybe you have used the probability counter on Deckstats and wonder what theory behind it is.

This introduction will not assume great knowledge about maths, but hopefully you can add, multiply and divide. A basic grasp of algebra is helpful too.

I will not provide proofs for anything, because I don't think it will help the target audience much. Each problem will have a motivation though, and be answered in a deductive form.

## About this guide
I am relatively new to Magic, and I'm no Euler, so it might contain both errors in regards to MtG and in regards to the maths involved.

If you spot an error please do get in touch and tell me.

## 1. The building blocks

### 1.1. How many different ways can we shuffle a deck?

Let us assume you have a magic deck of 40 cards.

Now, how many different ways can we shuffle these 40 cards? A lot, you say. That's true, but how many exactly?

We will shuffle our deck by spilling all the cards out on a table then picking one randomly, one after another.

Let's pick our first card. We have 40 cards to choose from. Then we have another 39 to pick from. Then another 38 and so forth. 

The crucial thing to understand now is that when we had picked our first card, for any card we picked as our first, there would be 39 to choose from for the next pick. This means that there is $40 \cdot 39$ ways to pick the first two cards in our sort.

You can look at it like you are along a trail, and at the first fork, you have 40 paths to chose from. The next one has 39 paths, and so forth. Everytime day, you walk this trail and change the path you take at some fork.

In total we have $$40 \cdot 39 \cdot \ldots \cdot 4 \cdot 3 \cdot 2 \cdot 1$$ ways to do this. This number is denoted $$40!$$ by mathematicians, and it's called the factorial. $$4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24$$ for example. The factorial of most numbers is usually a very large number. In fact, the number of ways to shuffle a 40 deck is *gigantic*:

$$40! = 815915283247897734345611269596115894272000000000$$

This may all seem very artificial and unrealistic, but we have introduced the factorial, which is a crucial tool later on.

#### But some cards are the same?

For the purposes of a random shuffle it doesn't matter. If you have 4 Pegasuses (Pegasii?), it's perfectly possible, from a probability standpoint that you get 4 of them next to each other.

### 1.2. How many different ways can we draw 7 cards from a completely unique 40 card deck?

Magic players are often encouraged to have multiples of some types of cards. This makes intuitive sense. More copies of the same creature, means a more consistent draw. But what if we eschewed this advice and had a 40 card deck where no card were the same. 

Armed with the factorial above, we know that there is 40, then 39, then 38, then 37, then 36, then 35 and finally 34 cards to possible cards at each step. So $$40 \cdot 39 \cdot 38 \cdot 37 \cdot 36 \cdot 35 \cdot 34 = \text{ALOT}$$. This number is enormous, not as enormous as the one above but still unfathomably large.

We can denote this number:

$$\frac{40!}{(7 - 1)!}$$

But how many possible starting hands are there? It doesn't matter if I draw 6 Forests and then a Ghalta or a Ghalta then 6 Forests. You would still say this is the same hand.

So in our number above, we have counted the same hand many times over. We can deal with this. How many ways can you arrange 7 cards? Let us rephrase that, how many ways can you shuffle 7 cards?

We know this! $$7!$$ So each possible hand is counted 7 times too much in $$\frac{40!}{(7 - 1)!}$$. We simply divide it by $$7!$$. Using common algebra this comes out as:

$$\frac{40!}{(7 - 1)! \cdot 7!}$$

This number is commonly referred to as the binomial number of 40 and 7. Sometimes we say "40 choose 7 without order", because we choose 7 of something from 40 items, and we don't care about the order.

$$\frac{40!}{(7 - 1)! \cdot 7!} = 224844379201911853600532206127677440000000$$

Oops, still enormous! But this number is actually many times smaller than $$40!$$. In the next session we will use this to actually calculate something useful!

## 2. Probabilities

### 2.1. The basics

### 2.2. Whats the probability we get one of our 1-drops in the first hand?
