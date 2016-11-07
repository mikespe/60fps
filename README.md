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
8. changed the constraint on the for loop (516) to 7 from 200, limiting the amount of elements that need to be changed by the 489 updatePositions function.
9. I wrote modified a script to include CSS into the page using javascript that way the CSS does not block rendering of the page, thus increasing the Google Pagespeed Insights score.
10. Optimized CRP by asyncing the javascript, removing the css link from the html and including it in the asynced JS

##Who doesn't like delicious pizza?

This site supports [this quiz](https://www.udacity.com/course/viewer#!/c-ud860/l-4147498575/e-4154208580/m-4142388616) from Udacity's [Browser Rendering Optimization](http://udacity.com/ud860)

This pizzeria site is a performance nightmare. Record a timeline trace and watch the Forced Synchronous Layout warnings pop up. Can you make this site run at 60fps?
