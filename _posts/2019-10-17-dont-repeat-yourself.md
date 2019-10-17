---
title: Don't Repeat Yourself?
featured_image: '/images/blog/dev_2.png'
tagline: When copy and paste is your friend.
---

![](/images/blog/dev_2.png)

When starting out as a developer, many learn early on not to repeat themselves. Out of the gate, this is inherently a great bit of advice to take to heart. Splitting up code into reusable components can have a multitude of benefits, such as increasing readability, testability, and ease of modification. This rule is often referred to as the "DRY" Principle (DRY of course, standing for "Don't Repeat Yourself"). However, sometimes the rules are meant to be broken, or at the very least, only considered as a guideline. 

The first exception to this rule is to allow repeating yourself when first writing a given piece of code. It's this point in time when copy and pasting is your ally. It's a common misconception to believe you understand the code you write as you're writing it. For most situations, this couldn't be further from the truth. It's often after the code has been written or a bug has been encountered that the code actually begins to be understood. Instead of trying to write an abstraction early on, before the implications of writing abstraction are fully understood, allow your code to be a bit un-DRY. Whenever writing code, if one piece of code mimics the functionality of another piece of code, it's perfectly fine to duplicate exiting code in order to understand what is happening. This more granular perspective can be very helpful - take a step back and compare the two pieces of code during the refactor and understand if a reusable abstraction is even necessary.

The other exception to allow your code to be un-DRY is when adding that abstraction makes it harder to modify rather than easier. Adding flexibility and adaptability to a reusable piece of code can sometimes result in an overly complex method that is difficult to understand and test. This can be the result of adding multiple configuration parameters (some of which may be optional) and branching conditional logic. In this case, there's two options: either more methods are needed, which then can be composed to create the necessary abstraction - or it simply ain't worth it and repeating yourself is totally fine. This is often the case when there is a high amount of variability in the ways that method is being called. The bottom line: if your method abstractions becomes too flexible, they can become overly complex. Complexity is bad. Just repeat yourself!

Is it easier to change code in two or more places than it is to modify a (potentially) complex abstraction? That's the tradeoff to be made.