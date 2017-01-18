## Website Performance Optimization portfolio project

####Part 1: Optimize PageSpeed Insights score for index.html
Pagespeed : 95 % Mobile; 96 % Desktop

1- Resized pizzaria.jpg to 100px 50px width.
2- Reduse the pizzaria size through an optimizer .
3- Add print media to print.css.
4- Inlined style.css.
5- Load google analytics async. 
6- Moved all javascript to the bottom of body tag.
7- Removed the link to fonts
 



####Part 2: Optimize Frames per Second in pizza.html

 views/js/main.js for pizza.html:

####In function changePizzaSizes(size):
    add new variable and remove the redunt 
   
    1-make variable randomPizzas outside the for loop so i don't need to querying to dom every time
    2-Changed querySelectorAll to getElementsByClassName
