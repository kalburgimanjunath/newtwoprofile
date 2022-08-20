---
published: false
layout: post
author: Manjunath
categories:
  - javascript
image: assets/images/6.jpg
tags: 'featured,stories'
---
#What is a Loop?
A Loop is a piece of code used in JavaScript to perform repeated tasks based on a condition. These conditions normally return a boolean value (true or false). A loop will continue running until the defined condition returns false.

Let's say you're tasked to write the number 1-100, you can either do this manually (which will definitely take a long time) or you can automate the process using a loop as shown below:

        for ( i = 0; i <= 100; i++) {
            console.log(i);
        }

There are various types of loops we can utilize in JavaScript. 

- while Loop
- do...while Loop
- for Loop
- for...in Loop
- for...of Loop

        while(condition) {
        //code to be executed
        }


        do {
          //code to be executed
        } while (condition)


        for (initialization; condition; iteration) {
        // code block to be executed
        }


for (key in object) {
  // code block to be executed
}

for ( let key in country ) {
    console.log(`${key} = ${country[key]}`);
}

for (variable of iterable) {
  // code block to be executed
}

for(const [key, value] of romanNumerals.entries()) {
  console.log(`${key} in Roman Numerals is  ${value}`);
}

That's it for this article.

If you found it useful, consider following me on Twitter and signing up for my weekly newsletter for more web developer content.