# kagi_task
Task for Kagi 

First task url:
https://kagi-task-repotools-projects.vercel.app/task_1.html

Second task url:
https://kagi-task-repotools-projects.vercel.app/task_2.html


<h1>Documentation on Implementations</h1>

<h2>Task 1, Example 1</h2>
<p>For Example 1, the method used to change CSS styles was by using a hidden checkbox input. Since we were already working with checkboxes, I found this to be a simpler solution.</p>
    <p>Then, I used the <code>nth-child</code> function to check the number of checkboxes inside the <code>&lt;li&gt;</code> element and determine whether to display the label with its corresponding text. If the hidden checkbox was checked, it would show "Show More"; otherwise, it would show "Show Less".</p>

<h2>Task 1, Example 2</h2>
<p>For Example 2, I could have also used a hidden checkbox, but I decided to take a different approach. I used the method of applying a class to the object based on the <code>target</code> applied to the <code>&lt;a href&gt;</code> elements, allowing me to show or hide the "Show More" or "Show Less" text.</p>
<p>The 10-line limit in this case restricted the line height to <code>1em</code>, and then I set the maximum height to 10 lines to ensure consistency across different browsers and screen sizes. When dealing with text, counting elements such as <code>&lt;p&gt;</code>, <code>&lt;h1&gt;</code>, <code>&lt;h3&gt;</code>, or <code>&lt;br&gt;</code> can vary significantly in size, meaning not every element will always represent a single line.</p>

<h2>Task 2</h2>
<p>For this task, the first thing I did was check the inputs and declare the necessary constants to determine when the function started. Then, I retrieved the input data and removed any spaces using <code>trim()</code>.</p>
<p>Next, I created the <code>people</code> array using the <code>split()</code> method and added the name at the end before sorting the array alphabetically with <code>sort()</code>, as it is more efficient than sorting using loops.</p>
<p>After that, I searched for the position of the name to determine the time it would take to reach my position. I declared the <code>endTime</code> constant to subtract from <code>startTime</code> and thus calculate how long the function execution took. Finally, I displayed the results on the screen.</p>

<h2>Corrections</h2>
<ul>
<li><strong>Task 1:</strong> After testing on different browsers, I found that the first example was not executing correctly. I resolved this by adding a container for the widgets and setting a <code>min-width</code> to prevent distortion on smaller screens, ensuring a horizontal scrollbar appears when necessary.</li>
<li><strong>Task 2:</strong> After testing <code>sort()</code>, I discovered that when names were entered in mixed case (uppercase and lowercase), they were not sorted correctly. To fix this, I added <code>toLowerCase()</code> to the inputs so that sorting works properly.</li>
<li>Additionally, when reviewing the issue of double spaces being counted as separate users, I could have made the function ignore blank names, but I chose to use <code>replace(/\s+/g, ' ')</code> to remove all double spaces, ensuring that there is only one space between names.</li>
<li>I also found that Safari does not correctly execute the <code>performance.now()</code> method, as it rounds milliseconds to the nearest whole number instead of displaying decimal values.</li>
</ul>
