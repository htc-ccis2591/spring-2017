---
title: "Practice Basic JavaScript"
published: true
morea_id: ex-basic-js-syntax
morea_type: experience
morea_summary: "Practice using basic javascript syntax."
morea_sort_order: 1
---

# Basic Javascript

## Goals
- Learn to make variables in Javascript
- Use string concatenation
- Use arithmetic operators
- Make an array and use array notation to access elements of the array
- Write a basic for loop
- Use a for loop to process the elements in an array

## Reading
Before beginning this assignment, you should read through chapters 3, 4, and 5 in the textbook to learn basic Javascript syntax.  You may also be interested in the functions which are written for you.  These are introduced in Chapter 6, and we will discuss those more in the next session.

## GitHub Info
Repository:  <https://github.com/htc-ccis2591-spring2017/basic-js-syntax>

You need to fork this repository and submit a pull request to turn in the assignment.  Please post a screenshot of the pull request to the D2L dropbox.  The dropbox is mainly used to communicate due dates, not for storing the completed work.  You do not need to upload the project to D2L, only to GitHub.

## Provided Files
Open the project (the basic-js-syntax folder) in Brackets (or your editor of choice). Remember when using Brackets, it is important to open the entire folder, not just a single file.

Look at the index.html file provided.  Notice that it includes a javascript file near the bottom.  It is generally considered a best practice to include your JavaScript files at the end of the HTML page to improve performance.  

If you are including more than one JavaScript file, the order that you include them is also important. The browser will run them in the order that you include them. This means that if one script depends on another (perhaps a library such as jQuery), the that dependent file must be included before the one that needs it.

Use the Brackets Live Preview feature to view the web page.  The output from the JavaScript will display in the console.  Open the Developer Tools and go to the JavaScript Console to see the output.
{% include img-medium.html url="/morea/hello-javascript/images/basic-js-initial-output.png"
   alt="Screenshot of initial program output in the browser console."
%}

## Assignment
Open the js/script.js file.  To complete the assignment, you will need to add JavaScript code as indicated in the comments. You're expected to write one line or block after each comment.  

In the assignment, you are expected to write messages to the console.  Use the console.log() function to do this.  The value you pass into the function (put between the parens) is what will be shown in the console.  That can be either a string (a message) or a value such as a number or an array.  

The code provided for you at the bottom will call the functions for you one at a time. It is important that you do not remove any of the starter code or change the names of the functions.  If you do so, the code may no longer run correctly.

When the assignment is complete the output should look something like this:
{% include img-medium.html url="/morea/hello-javascript/images/basic-js-final-output.png"
   alt="Screenshot of final program output in the browser console."
%}


## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Go to your repository settings, and locate the URL where the page is published.  Copy this URL.
{% include img-medium.html url="/morea/hello-javascript/images/basic-js-get-test-url.png"
   alt="Screenshot of showing GitHub Settings location for published web page."
%}

Go back to the repository view and edit the description. Paste in the URL in the space for the website.  
{% include img-medium.html url="/morea/hello-javascript/images/basic-js-edit-repo-desc.png"
   alt="Screenshot of showing how to update repository description on GitHub."
%}

Click the link to view the page and make sure that it runs correctly.  

After you have verified the page is working, create the pull request to submit the assignment.  Take a screenshot of both your console output from your page running on GitHub and your Open pull-request to put in the assignment dropbox.
