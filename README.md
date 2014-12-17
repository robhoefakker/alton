# README #
**Name:** featured-scroll.js

**Version:** 1.0

**Author:** Paper Leaf

**Author Website:** http://www.paper-leaf.com

**Description:** A full featured scrolling plugin for creating immersive featured sections or headers.

**Copyright 2014 Paper Leaf Design**


## Credit ##
### is_mobile() Credit ###
is_mobile() based off these helpful posts
- http://stackoverflow.com/questions/3514784/what-is-the-best-way-to-detect-a-handheld-device-in-jquery
### Scroll Event Stabilization ###
Getting stable scroll events was helped hugely by Huge Inc's insights
- http://www.hugeinc.com/ideas/perspective/scroll-jacking-on-hugeinc
### Keyboard Events Stabilization ###
Stabilizing keypress events was helped in large part by jQuery OnePage Scroll
- https://github.com/peachananr/onepage-scroll

## Use Cases ##
There is a couple of features that this plugin covers.

To start things off here's every option that is available and it's default

```
#!javascript
$(document).scrollJack({
    firstClass : 'header', // classname of the first element in your page content
    fullSlideClass : 'full', // full page elements container for 
    nextElement : 'div', // set the first element in the first page series.
    previousClass : null, // null when starting at the top. Will be updated based on current postion
    lastClass: 'footer', // last block to scroll to
    slideNumbersContainer: 'slide-numbers', // ID of Slide Numbers
    bodyContainer: 'pageWrapper', // ID of content container
    scrollMode: 'featuredScroll', // Choose scroll mode
    useSlideNumbers: false, // Enable or disable slider pagination
    slideNumbersBorderColor: '#fff', // Choose pagination bullets border color
    slideNumbersColor: '#f8f8f8', // Choose pagination bullets fill color
    animationType: 'cubic-bezier(2.63, 2.64, 2, 2)', // Choose animation style
});
```

### Featured Scroll. ###
The Idea behind featured scroll is that you have a header and footer section with a featured area of projects or something in the middle. 

### Header Scroll ###
The Idea behind header scroll is that you have a featured header area, that on scroll disappears, an you find yourself at the main content, with native scrolling enabled.

Here is an example for all the options available for headerScroll:

First ensure you have the proper HTML structure:

```
#!html

<section class="header">
<!-- Insert Header Content Here -->
</section>
<section class="pageWrapper">
<!-- Insert Regular Content Here -->
</section>
```


```
#!javascript

$(document).scrollJack({
    firstClass : 'header', // classname of the first element in your page content
    bodyContainer: 'pageWrapper', // ID of content container
    scrollMode: 'headerScroll', // Choose scroll mode
    animationType: 'cubic-bezier(2.63, 2.64, 2, 2)', // Choose animation style
});
```