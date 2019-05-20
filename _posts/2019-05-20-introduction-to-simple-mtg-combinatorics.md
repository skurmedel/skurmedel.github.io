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

You can look at it like you are along a path, and at the first fork, you have 40 paths to chose from. The next one has 39 paths, and so forth.

In total we have $40 \cdot 39 \cdot \ldots \cdot 4 \cdot 3 \cdot 2 \cdot 1$ ways to do this. This number is denoted $40!$ by mathematicians, and it's called the factorial. $4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24$ for example.

This may all seem very artificial and unrealistic, but we have introduced the factorial, which is a crucial tool later on.

#### But some cards are the same?

For the purposes of a random shuffle it doesn't matter. If you have 4 Pegasuses (Pegasii?), it's perfectly possible, from a probability standpoint that you get 4 of them next to each other.

### 1.2. How many different ways can we draw 7 cards from a 40 card deck?

## 2. Probabilities

### 2.1. The basics

### 2.2. Whats the probability we get one of our 1-drops in the first hand?
