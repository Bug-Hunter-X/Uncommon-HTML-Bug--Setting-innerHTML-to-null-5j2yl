# Uncommon HTML Bug: Setting innerHTML to null

This repository demonstrates an uncommon bug in HTML related to setting the `innerHTML` property of an element to `null`.  The issue is inconsistent across different browsers.

## Bug Description

The bug involves setting the `innerHTML` property of a div element to `null`. In some browsers, this unexpectedly leaves the previous content visible, even though the DOM element is technically empty. Other browsers will behave as expected and clear the content.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe the behavior of the div element.  You might see the text remaining visible despite the script attempting to clear it.

## Solution

The solution is to set the `innerHTML` to an empty string ("") instead of `null` to consistently clear the content across all browsers. See `bugSolution.html` for the fix.

## Note

This bug highlights the importance of consistent coding practices.  While `null` might seem like a logical way to clear content, it can lead to unexpected browser-specific behaviors.