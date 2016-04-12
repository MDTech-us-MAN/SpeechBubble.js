# SpeechBubble.js

This library makes it easy to display a Speech Bubble above an element!

## Usage

#### Create a Speech Bubble
```javascript
var SpeechBubbleDiv = SpeechBubble(document.getElementById('MyElement'), 'This is my bubble's content.', 'MyBubbleClass');
```
The `SpeechBubble` function returns the `<div>` that it created and adds it to the `window.OpenSpeechBubbles` array.

#### Close a Speech Bubble
```javascript
SpeechBubbleDiv.removeBubble();
```
**NOTE:** The `.removeBubble()` function is the _ONLY_ correct way to remove the bubble.

#### Close all open Speech Bubbles
```javascript
OpenSpeechBubbles.forEach(function(bubble) { bubble.removeBubble(); });
```

## Dependencies
##### None. There are no dependencies.

## Things to note
* **The element you specify should have a fixed width.**  
   Otherwise, the bubble will end up pointing at the middle of the page.

* **For IE 8 support, please include the `addEventListener` polyfill.**  
   https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#Compatibility
