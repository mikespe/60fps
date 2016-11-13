#Summary

This project was done to demonstrate the optimization of a website to 60 fps

#Changes made
1. Javascript Minification
2. CSS Minification
3. Image Compression and resizing
4. Removed function determineDx (425) from main.js
5. Edited function changePizzaSizes(451) by removing dx, putting dom selection into a variable, moving the queryselector outside the for loop, and then removing line 454 newwidth variable in the forloop and inporated it in the 431 switch statement
6. Removed function sizeSwitcher (431) and made the switch the beggining of the nwe ChangePizzaSizes which initially has the switch statement, then reads the randompizzas, then iterates through them changing the width, avoiding layout thrashing.
7. Fixed function updatePositions (489) by moving the phase variable to before the for loop at (495)
8. changed the constraint on the for loop (516) to 24 from 200, limiting the amount of elements that need to be changed by the 489 updatePositions function.
9. I wrote modified a script to include CSS into the page using javascript that way the CSS does not block rendering of the page, thus increasing the Google Pagespeed Insights score.
10. Optimized CRP by asyncing the javascript, removing the css link from the html and including it in the asynced JS
11. line 461 function i moved pizzasDiv outside the for loop
12. added transform and backface-visibility to .mover in css
13. replaced the dom element selection on 526 with movingpizza

##How to run

1. Download the repository
2. Extract all to your documents directory
3. Double Click the index.html file and run in the browser
