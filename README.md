# Incorrect usage of textContent vs. innerHTML in HTML

This repository demonstrates a common yet subtle error in HTML when manipulating the content of an element.  The difference between `textContent` and `innerHTML` can lead to unexpected behavior and security issues if not understood.

## Bug Description
The `bug.html` file attempts to update the content of a `<div>` element using `textContent`. However, if you're trying to insert HTML directly, this will not work as expected.

## Solution
The `bugSolution.html` file showcases the correct way to use `innerHTML` when you intend to inject or modify HTML within an element.

## Learning Points
* **`textContent`**: This property sets or gets the textual content of an element, ignoring any HTML tags.
* **`innerHTML`**: This property sets or gets the HTML content of an element.  Use with caution, as it's prone to XSS vulnerabilities if not properly sanitized.

Always sanitize user input before using `innerHTML` to prevent Cross-Site Scripting (XSS) attacks.