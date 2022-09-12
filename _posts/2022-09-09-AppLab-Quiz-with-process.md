---
toc: true
layout: post
comments: true
description: A review process of utilizing AppLab.
categories: [markdown]
title: AppLab Quiz with thought proccess 
--- 

- Link to my quiz:https://studio.code.org/projects/applab/soa85epSNrnMgUSUzoqjz6_02hq4_5rXXS_Od-6BooM

- Link to the control source for my quiz:https://studio.code.org/projects/applab/rEkq6_-HMk-W8WkN1WoZFm45pdGoioqK4ur9sYYve6Q

- This week, we were responsible for making our own 3 question quiz with Code.org's AppLab. In this post, I will include the finished quiz, and go through my thought process as I made it 

- Starting off, we were shown a example quiz about golf, and we were able to see the building blocks that made it work, then we were promptly shown the Applab itself, which utilizes coding and design elements in order to run projects. 

- Using the example quiz's code as a control, I would frequently look at it for reference to code, while using the design element to alter how the project would look, placing buttons, typing text, and overall make the quiz look aesthetically pleasing as it was functional

- Then came coding. There were dozens of code blocks that had their own unique functions, but I primarily used the event block, which would output a value whenever an event took place, like clicking a button or pressing a key on your keyboard. So I would take this block, alter the id so it would respond to whenever a certain button was pressed

- If the button pressed was the correct answer, the next screen with the next question is displayed. If it was an incorrect result, then you'd be taken to a 'Game Over' screen, and can press a button that allows you to try the quiz again (Setting the screen to the first question)

- I repeated this until I had 3 questions, with 3 right answers and 9 wrong answers. Then I designed the final screen with 2 buttons, one that allows you to take the quiz again, and the other... We'll get to that in a bit. 

-So there was a lot of trial and error, but the most primary of which was attempting to code everything without utilizing the design feature, which was a necessity. Suffice to say, trying to make a quiz with only the code feature was a tough process until I properly utilized design (I originally couldn't make one question) 

- Now..we have some added elements 

- For Screen 2, you have the option to press a button, and doing which will take you to one of the best music videos to exist. I did this by inputing the "open url" block into the event block, and then inserting the url to the video in the prompt asking for it, and upon running, it would successfully take any person who clicks it, watch the video

- Alas if you care not for what the button brings, then you can continue, but there isn't any button to press that moves you on with the quiz. Instead, you can simply press any key you want to go to the quiz. This element was utilized by the same event block, but instead of recognizing the button press, it would only recognize if a key was pressed, and then the output of which would be mkoving you to the next screen, beginning the quiz

- Thank you for embarking on this long read, I hope you enjoyed