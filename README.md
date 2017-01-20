# Website Performance Optimization portfolio project

*Auther:* Asmaa Hassan
*Date:* January 19, 2017

##Description:
This project is part of Udacity FrontEnd nanodegre, the outcome of the project is Optimizing a website code. The original code was running at less than 60 fps while scrolling, as well as slow pizzas rezsizing. After the my modification to the code, the webpage is running at 60 fps or higher and we have better preformance when resizing the pizzas.


##Project Instruction:
###Data Collection
- You can read the project requirements at the following url:
https://review.udacity.com/#!/rubrics/16/view

- To get started please download the original non optimize code from the following repository:
https://github.com/udacity/frontend-nanodegree-mobile-portfolio


###Code Optimization steps
####Part 1:
- The first part of the project is to optimize PageSpeed Insights score for index.html
- The following steps is required in order to meet the requirements

*Affected files:*
- pizza.html
- index.html
- print.css
- style.css

1- make another copy of pizzeria.jpg the same size for pizza.html. 
2- Resized pizzaria.jpg to 100px 50px width. the small copy for index.html.
2- Reduse the pizzaria size through an optimizer .
3- Add print media to print.css.
4- Inlined style.css.
5- Load google analytics async. 
6- Moved all javascript to the bottom of body tag.
7- Removed the link to the fonts.

Confirm the phade by testing via the PageSpeed Tools 


####Part 2:
- The second part of the project is to optimize the fps for pizza.html
- As per the requirements the fps must be 60 fps when scrolling, 
- And reduce the time to resize the pizzas via the slider to less than 5 ms, 
- The following steps is required in order to meet the requirements

*Affected files:* 
- views/js/main.js

1- Move the variable randomPizzas outside the for loop, so dom is not queryed every time.
3- Use getElementsByClassName() instead of querySelectorAll to speed up the query selections.
4- Move the variable pizzasDiv outside the for loop to reduse the redundancy and to speed up the code.
5- Move document.body.scrollTop outside the for loop, and to speed the animation store document.body.scrollTop in new variable called dbs and reuse it inside the loop.
6- declare the variable phase outside the for loop.
7- Reduce the number of pizza (reduse the for loop from 200 to 32);
9- Declare the variable elem outside the for loop.
