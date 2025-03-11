# kagi_task
Task for Kagi 

First task url:
https://kagi-task-repotools-projects.vercel.app/task_1.html

Second task url:
https://kagi-task-repotools-projects.vercel.app/task_2.html


Documentation on Implementations
- Task 1, Example 1:

For Example 1, the method used to change CSS styles was by using a hidden checkbox input. Since we were already working with checkboxes, I found this to be a simpler solution. Then, I used the nth-child function to check the number of checkboxes inside the <li> element and determine whether to display the label with its corresponding text. If the hidden checkbox was checked, it would show "Show More"; otherwise, it would show "Show Less."

- Task 1, Example 2:

For Example 2, I could have also used a hidden checkbox, but I decided to take a different approach. I used the method of applying a class to the object based on the target applied to the <a href> elements, allowing me to show or hide the "Show More" or "Show Less" text. The 10-line limit in this case restricted the line height to 1em, and then I set the maximum height to 10 lines to ensure consistency across different browsers and screen sizes. When dealing with text, counting elements such as <p>, <h1>, <h3>, or <br> can vary significantly in size, meaning not every element will always represent a single line.

- Task 2:

For this task, the first thing I did was check the inputs and declare the necessary constants to determine when the function started. Then, I retrieved the input data and removed any spaces using trim(). Next, I created the people array using the split() method and added the name at the end before sorting the array alphabetically with sort(), as it is more efficient than sorting using loops. After that, I searched for the position of the name to determine the time it would take to reach my position. I declared the endTime constant to subtract from startTime and thus calculate how long the function execution took. Finally, I displayed the results on the screen.

Corrections:
Task 1: After testing on different browsers, I found that the first example was not executing correctly. I resolved this by adding a container for the widgets and setting a min-width to prevent distortion on smaller screens, ensuring a horizontal scrollbar appears when necessary.

Task 2: After testing sort(), I discovered that when names were entered in mixed case (uppercase and lowercase), they were not sorted correctly. To fix this, I added toLowerCase() to the inputs so that sorting works properly. Additionally, when reviewing the issue of double spaces being counted as separate users, I could have made the function ignore blank names, but I chose to use replace(/\s+/g, ' ') to remove all double spaces, ensuring that there is only one space between names. I also found that Safari does not correctly execute the performance.now() method, as it rounds milliseconds to the nearest whole number instead of displaying decimal values.
