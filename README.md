#Summary

This project was done to demonstrate the optimization of a website to 60 fps

#Changes made to pizza.html
1. Javascript Minification
2. CSS Minification
3. Image Compression and resizing
4. Removed function determineDx (425) from main.js
5. Edited function changePizzaSizes(451) by removing dx, putting dom selection into a variable, moving the queryselector outside the for loop, and then removing line 454 newwidth variable in the forloop and inporated it in the 431 switch statement
6. Removed function sizeSwitcher (431) and made the switch the beggining of the nwe ChangePizzaSizes which initially has the switch statement, then reads the randompizzas, then iterates through them changing the width, avoiding layout thrashing.
7. Fixed function updatePositions (489) by moving the phase variable scroll finder and dom selection into a variable above the for loop.
8. changed the constraint on the for loop (516) to 24 from 200, limiting the amount of elements that need to be changed by the 489 updatePositions function.
9. I wrote modified a script to include CSS into the page using javascript that way the CSS does not block rendering of the page, thus increasing the Google Pagespeed Insights score.
10. Optimized CRP by asyncing the javascript, removing the css link from the html and including it in the asynced JS
11. line 461 function i moved pizzasDiv outside the for loop
12. added transform and backface-visibility to .mover in css
13. replaced the dom element selection on 526 with movingpizza
14. line 441 replaced querySelectorAll with getElementByClassName.

#Changes made to index.html
1.  exported analytics js script to external async file - no more blocking the rendering;
2.  added media='print' to print.css - only gets downloaded if the person wants to print, removing from crp
3.  inlined style.css - removes fetching from crp
4.  added async to any possible external js scripts - removes from crp and executes last
5.  resized a couple images - lowered KB
6.  compressed images - lowered KB
7.  minified css and js - lowered KB
8.  moved font data uri to css using @font-face - removed fetching and blocking of crp


##How to run

1. Download the repository
2. Extract all to your documents directory
3. Double Click the dist folder then the index.html or the pizza.html file inside the views directory and run in the browser.
