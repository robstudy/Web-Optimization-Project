Original repository for site https://github.com/udacity/frontend-nanodegree-mobile-portfolio

To run the application you all you need do is open index.html and navigate through the pages.

Optimizations:

1. Index.html, project-2048.html, project-webperf.html, all include inclined, minified, css, and no longer link to external css files(for faster loading).

2. All image files have been compressed using ImageOptim, which can be found at (https://imageoptim.com/). Images that were too big were resized for their displays.

3. Javascript for these pages have been made async to keep them from render blocking.

4. Pizza.html now has inlined, minified, style.css but keeps bootstrap-grid.css as a external link. bootstrap-grid.css has been minified.

5. Added viewport meta tag to pizza.html

5. all javascript files except main.js have been made async.

Main.js Changes:

1. Only 32 sliding pizzas are created instead of 200. That many pizzas do not need to render.

2. Created an array called moverArray to store each sliding pizza object, instead of pulling each object by ID and for loop, now we only need to iterate through the moverArray[].

3. body.scrollTop call and phase variable moved outside of the for loop for scrolling.

4. Removed all instances of document.querySelectorAll() wutg document.getElementsByClassName().

5. In changePizzaSizes placed randomPizzas outside of for loop. Used switch() to change pizza sizes width and removed determinedx as it was no longer a needed function.