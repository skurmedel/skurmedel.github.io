---
layout: post
title: A nitpicky explanation of sRGB gamma correction
tags: [graphics, colour, math]
category: computer graphics
---

## What is sRGB?
sRGB is a colour space, and a standard that is probably the most common colour space for computer displays. 

## Why do we gamma correct? 
Here are some good explanations:

  - http://www.cambridgeincolour.com/tutorials/gamma-correction.htm
  - http://www.cgsd.com/papers/gamma_intro.html
  
*In the future I wish to put together an artist-friendly explanation with some interactive aids to explain the whole idea behind a linear workflow.*

## The power function
Now, after reading the above two links, you might think that gamma correction is simply raising each pixel p:s value by some number:
$$p^{2.2}$$ and undoing the operation is simply $$p^{1/2.2}$$.

As I'll explain, for sRGB, this is not really correct. It works, but it is an approximation. If you want to be compliant with the standard, you need to use the functions below, which you'll note is actually a piecewise function.

## Linear to corrected

blabla

$$\begin{cases}
12.92C_\mathrm{linear}, & C_\mathrm{linear} \le 0.0031308\\
(1+a)C_\mathrm{linear}^{1/2.4}-a, & C_\mathrm{linear} > 0.0031308
\end{cases}$$

## Corrected to linear

## The reasoning behind the piecewise function

## Using 2.2 as an approximation

### Comparisons

## GLSL code

## Note about Rec709 and Rec2022
