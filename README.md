# Uncommon HTML Bug: DOM Element Access Before Load

This repository demonstrates a common error when working with JavaScript and the DOM in HTML.  The bug occurs when attempting to access and manipulate a DOM element before it has been fully parsed and loaded into the browser's Document Object Model (DOM).

## The Bug
The `bug.html` file contains a simple HTML page with a script that attempts to access a `<div>` element and modify its inner HTML. If the script runs *before* the `<div>` element is fully loaded into the DOM, it will result in a `TypeError` (or a similar error) because `document.getElementById("myDiv")` will return `null`.

## The Solution
The `bugSolution.html` file presents a solution which demonstrates how to avoid the error by either delaying the script or by checking if the element exists before attempting to manipulate it.  The better approach is to always check the existance of the element before manipulating it.