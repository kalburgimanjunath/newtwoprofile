---
layout: post
title: How to create Filter / search in reactjs
author: manjunath
categories:
  - tutorial
image: assets/images/6.jpg
tags: featured
published: true
---
Created a player which displays videos from many sources and with this tool you can only focus on value added videos.
Let me tell you how to create simple filter like google in reactjs. I have used stackblitz to react the project its pretty simple go to stackblitz and select react javascript project you will land into the react javascript project.

![image](https://miro.medium.com/max/1400/1*4FWhtNxeu3XvEWeA4DSFfA.png)
Once clicked react(javascript) your project folder looks like this.
![image](https://miro.medium.com/max/700/1*8Whh2DN-SrAYRCs6Qm9MOA.png)
Create components folder to add your components and css for holding your css. Open App.js and edit the file. 
![image](https://miro.medium.com/max/700/1*zm_qyT8DXfDhHy91p3vRKQ.png)
Add following code
![image](https://miro.medium.com/max/623/1*q833u8FQ4wBusWob4CIRug.png)
Let me explain you what I have did, Added BrowserRouter for Link tag and added Element Added Search component.

### Part 2.
Create 2 files in components folder Search with Search.js Avatar with Avatar.js to hold user information
![]({{site.baseurl}}/https://miro.medium.com/max/510/1*XgCeUrHMLpyZQTy5n7dHHA.png)
## Search with search.js
![]({{site.baseurl}}/https://miro.medium.com/max/593/1*CET-OAjQtJBOcN12ZuF_sw.png)
Let me explain the code, created users array to hold the users api data and player to hold the search box data. I am using UseEffect react hook to fetch the data from API and setting up that in users array object with setUsers function. onChange store my search parameter inside player variable with setPlayer function. Final part to render my html and values
![]({{site.baseurl}}/https://miro.medium.com/max/628/1*ttNG9-dUYXCY2_G2T2L6TA.png)

Final result looks like this. https://react-d1dyj6.stackblitz.io

![]({{site.baseurl}}/https://miro.medium.com/max/408/1*e3ZzAI3-RaAIIjrncnHbXQ.png)
