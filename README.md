# Website Performance Optimization portfolio project

*Auther:* Asmaa Hassan
*Date:* January 19, 2017

##Description:
This project is part of Udacity FrontEnd nanodegre, the outcome of the project is Optimizing a website code. The original code was running at less than 60 fps while scrolling, as well as slow pizzas rezsizing. After the my modification to the code, the webpage is running at 60 fps or higher and we have better preformance when resizing the pizzas.
Also the project requires index.html to reach a Google Pagespeed Insights score of 90 or above.


##Project Instruction:
###Data Collection
- You can read the project requirements at the following url:
https://review.udacity.com/#!/rubrics/16/view

- To get started please download the original non optimize code from the following repository:
https://github.com/udacity/frontend-nanodegree-mobile-portfolio


###Code Optimization steps:
####Part 1:
- The first part of the project is to optimize PageSpeed Insights score for index.html
- The following steps is required in order to meet the requirements

*Affected files:*
- index.html
- print.css
- style.css

1- Optimized images: 
 - Resized and reduce  pizzaria.jpg and use the small copy for the index.html .

2- Inline CSS styling: 
 - Add print media to print.css.
 - Inlined style.css.

3- Eliminate render-blocking JavaScript:
 - Moved all javascript to the bottom of body tag.
 
4- Load google analytics async. 
5- Removed the link to the fonts.

Confirm the phade by testing via the Google PageSpeed Tools .



####Part 2:
-The second part of the project is to optimize the fps for pizza.html
-As per the requirements the fps must be 60 fps or higher when scrolling, 
-And reduce the time to resize the pizzas via the slider to less than 5 ms, 
-The following steps is required in order to meet the requirements

*Affected files:* 
-views/js/main.js .
First record the timeline and Identify where Forced Synchronoused Layout in Main.js then apply the folloing steps: 

1-Moved DOM queries out of loops where applicable ,so dom is not queryed every time to reduse the redundancy and to speed up the code
-Move the variable randomPizzas outside the for loop.
-Move the variable pizzasDiv outside the for loop.
-Declare the variable elem outside the for loop.
-Declare the variable phase outside the for loop.
2-Changed all querySelectors into getElementById or getElementsByClassName to speed up the query selections.
3-Optimized pizza slider calculations.
4-Move document.body.scrollTop outside the for loop, and to speed the animation store document.body.scrollTop in new variable called dbs and reuse it inside the loop.
5-Changed number of pizzas rendered from 200 to the minimum needed (32).
