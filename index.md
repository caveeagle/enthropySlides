---
title       : Shannon Entropy
subtitle    : 
author      : Efremov Victor
job         : Data Science
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      #
logo        : entropy.png
widgets     : [mathjax, bootstrap, quiz] # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

--- .class #id 



## How random is your password?

When I needed to calculate the randomness of strings set (for data security tasks), I could not find suitable functions in R, calculating the entropy of string. So I created an R package and application that calculates the entropy [(a measure of information)](https://en.wikipedia.org/wiki/Entropy_%28information_theory%29), based on the analysis of the frequency of occurrence of characters in a block of text.

Application usage:

- Know how random is your password
- Calculate the amount of information contained in the text
- See what is the Shannon entropy like and how it changes when we change the frequency of characters in a string

---
## What is Shannon entropy?

The entropy $H$ and the amount of the information $I$ depend on the initial amount considered variants N and a priori probabilities of each implementation. Calculation of entropy in this case, according to the formula of Shannon, which proposed in 1948 in the paper ["Mathematical Theory of Communication"](http://worrydream.com/refs/Shannon%20-%20A%20Mathematical%20Theory%20of%20Communication.pdf), is:

$$H(X)= - \sum_{i=1}^np(x_i)\log_b p(x_i)$$

Shannon entropy is the average characteristic - the expectation value of the distribution of random variable ${I_0, I_1, ... I_N}$, and can be used as a measure of information uncertainty.

**_Note: Sorry for my bad English..._**

---

Let's see how the entropy changed when we changed type of text: 

| String        | Entropy   | Explanation        
| ------------- |:-------------:| -------------:|
| `To be, or not to be: that is the question...`      | 3.677531 | Normal text string
| `YoXl49oYQgtfDFOLMPXxzOBrhB4dLDuatOdm5Neikebu`      | 4.851366 | Autogenerated random password
| `qwertyuiopasdfghjklzxcvbnm1234567890QWERTYUI`      | 5.4594316 | Set of recurrent charters

![](empty.png)

Some **real** passwords, and it's autogenerated equivalent with the same length:

| Real password | Entropy   | Equivalent | Equivalent entropy         
| ------------- |:-------------:| -------------:| -------------:|
| `heybuddy`    | 2.5 | `BKZlMvTr` | 3
| `austinschuster`    | 3.1820058 | `Uzrw3IzsEXahHt` | 3.6644978
| `likearolingstone`    | 3.375 | `BH3vLWNpddSJom1L` | 3.75
| `20010187`    | 2.1556391 | `4pJFxMoU` | 3
| `ololol`    | 1 | `9EehfG` | 2.5849625

*(all entropy values on this page contain embedded R code, that got evaluated)*

--- &radio

This presentation for my [Application](https://caveeagle.shinyapps.io/shinyApp) is create as a part of a course project "Developing Data Products" on specialization "Data Science". For all questions, please contact me by mail: caveeagle@mail.ru

![](empty.png)
![](empty.png)

Did you like the presentation?

1.    _Yes_
2.    No

*** .hint 
Of course, Yes!

*** .explanation 
Yes! (because I tried very hard)






















