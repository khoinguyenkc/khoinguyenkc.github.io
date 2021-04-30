---
layout: post
title:      "Javascript: Alchemy of the modern internet"
date:       2021-04-30 03:35:51 +0000
permalink:  javascript_alchemy_of_the_modern_internet
---


I've heard somewhere that to understand how something is built, break it. That is one way to do it. A close analogue is probably to understand how something is built, build it. Building an app through vanilla Javascript without a framework has been quite educational. We can take frameworks like React for granted, but experiences like this is what makes us appreciate all the lifting that React does for you, and all the problems it helps you avoid. Since you are doing everything manually, you get an insider perspective of what goes into building a UI. This post will highlight the differences between React and vanilla Javascript. 


THE TEDIOUS TASKS
Here is an incomplete collection of decisions you might need to make and tasks you might need to do as you are building websites in vanilla Javascript.

Whether to store all data in some global/local boject - or pass relevant data to the relevant functions only, like a chain of hot potatoes. 
Where in the code to add to DOM the content
How you hide a button as it is clicked
How you build the "grid" of div elements with id/class names so you can later add content inside them.
Creating references for DOM elements
Removing the current content and shows the previous content should the user wants to go back/cancel the current task...
Freezing other functionalities
Clear "competing" content before you render new content (ex: imagine Facebook messenger, clear the old message as user wants to see the detail of the new message.

Often in our minds, we think of Javascript as document.createElement, adding listeners, appending nodes, query selecting nodes, removing nodes. But in practice, the bulk of our time is spent doing the invisible work above. 


SEEING THE BIG PICTURE
Some of the above tasks turns out harder than it looks. And one very big reason for that is that, in JS, we are unable to see the big picture. In React, everything is a component. You can visualize what this component looks like once it's mounted. 

On the other hand, in Javascript, all you see is is a DOM node appended to a parent DOM node. That's now a realistic picture. You would have to go out of your way to see what the final html of this "component" will end up looking like in JavaScript. 

One solution to that is literally you sketching out the HTML first before you try to "translate" it into JS. This is something I only realized in hindsight upon much reflection. The idea to implement HTML-looking JSX in React is just underrated pure genius. You can look at a React component's render function and are able to visualize things much easier.


DIVIDING THINGS UP
Another trap for newbies in JS is to not breaking things into small, independent units. What does that mean? There are usually groups of function that serve each "component". Example: Store data, render button, remove button, add content to DOM, add listeners, extract data, fetch data, receive data and rerender content accordingly. And you can group them in however you want.  Make them methods inside a class or, informally, just put them in a separate file. As long as there is a mental and visual separation. A classic mistake is to think "I will organize this when I'm done". But the problem is, the mess is sitting there as you are trying to be "done", which makes it very hard to get things, well, done.

In contrast, let's look at React. The cool thing about React is that the use of components automatically force u to divide things up. All the relevant methods in a React component is is defined within it, or in its prop.
And it goes even further than that. React components tend to be very small, and nested inside container components. In vanilla JS, there is nothing to enforce you. It's very easy to unwittingly try to add a large chunk of HTML into the DOM, and then have another function to manage all the interactions from that chunk of code. Things quickly get out of hand. You don't see the mess until you created that mess. 

Divide and conquer is unglamorous, but I find it to be the number one thing for tackling any substantial challenge. 


CONCLUSION

Comparing vanilla JS with React makes me realize how much more thought you have to put in when using vanilla JS - a staggering amount. React probably takes at least 80% of that work off your shoulders. It still baffles me to think how much work is reduced in React. React not only abstracts away many tedious tasks like removing and adding to the DOM, but it also does some mysterious voodoo! It whispers in your ears and bring out the better angels of our nature. Let me explain that in a second.

If you write good code in JS, you start to notice it resembles React. But it takes lots of knowledge and discipline to do that on your own. React FORCES you to do that. React is insidious, but authoritarian, in the way it enforces discipline on you. And the result is - you write clean, modular, manageable code.

At the end of the day, of course you can just use React and never look back at vanilla JS again. But it feels a bit like relying on your car and refusing to learn how to walk. It's a crutch. I believe it's important to examine the inner machinery. If React was an Ikea table, Javascript is carpentry. And I think knowing how it's made will make you a better builder in the end.


