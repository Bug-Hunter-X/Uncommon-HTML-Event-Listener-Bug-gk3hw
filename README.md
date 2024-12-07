# Uncommon HTML Event Listener Bug
This repository demonstrates a subtle bug in HTML event handling that might not be immediately obvious to developers.  The issue centers around how event listeners are attached to elements and how event propagation works.

## Bug Description
The `bug.html` file shows an incorrect method of adding an event listener.  It directly attaches the listener to the target element, but doesn't account for event bubbling.  This causes the `alert` to not trigger when the div is clicked.  The `bugSolution.html` demonstrates the correct implementation that will fire the event.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Click the div. Note that the alert doesn't show.
4. Open `bugSolution.html`.  Click the div. The alert should show.

## Solution
The solution involves understanding event bubbling and using the `document` as the target for the event listener and checking if the element clicked is the one we want to target.

This example highlights the importance of understanding the event propagation model in JavaScript when working with HTML.