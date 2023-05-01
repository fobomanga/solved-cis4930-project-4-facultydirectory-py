Download Link: https://assignmentchef.com/product/solved-cis4930-project-4-faculty_directory-py
<br>



<h1>1           faculty_directory.py</h1>

Suggested modules: requests, lxml or re

In this part of the assignment, your job is to create a script that will navigate to the FSU CS department website and print out a directory containing the telephone number, office location, email, and webpage of every faculty member in the department. The root page for the faculty listings is <a href="https://www.cs.fsu.edu/department/faculty/">http://www.cs.fsu.edu/department/faculty</a><a href="https://www.cs.fsu.edu/department/faculty/">/</a><a href="https://www.cs.fsu.edu/department/faculty/">.</a>

From this page, you can find links to every individual faculty page. Each individual faculty page lists the links that you need. <em>However, the only link that you may hardcode into your file is the one above</em>. <em>You also may not hardcode faculty names. </em>All other information from this point must be retrieved using crawling and scraping methods. Here is some guidance:

<ol>

 <li>First, try to gather all of the links to the individual faculty pages.</li>

 <li>Navigate to the first page and scrape the data to be output to the user.</li>

 <li>Repeat step 2 until all faculty information has been output to the user. An example of what your output should look like is shown below.  Missing information should be indicated with an “N/A” entry. Be careful of edge cases or inconsistencies, you may need to be a little creative – double check your output against the web pages!</li>

</ol>

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="6c0f0d05180005022c1c15010d0f04050209">[email protected]</a>$ python faculty_directory.py

Name:  Sudhir Aggarwal

Office:  263 Love Building

Telephone:  (850) 644 0164

E-Mail:  sudhir [ at cs dot fsu dot edu ]

****************************************

Name:  Theodore Baker

Office:  N/A

Telephone:  N/A

E-Mail:  baker [ at cs dot fsu dot edu ]

****************************************

Name:  Mike Burmester

Office:  268 Love Building

Telephone:  (850) 644-6410

E-Mail:  burmeste [ at cs dot fsu dot edu ]




…

<h1>2           imgur_info.py</h1>

Suggested modules: requests, json




Your job in this part of the assignment is to sort through Imgur user comment data. Your program should begin by prompting the user to enter a username of an Imgur account.




An Imgur user page can be found at http://imgur.com/user/&lt;username&gt;, but the comments on this page are loaded dynamically which can make it very hard to pull data. The dynamically loaded content, however, is systematic and easy to retrieve. All of the user’s comments can be found at




http://imgur.com/user/&lt;username&gt;/index/newest/page/&lt;num&gt;/hit.json?scrolling




where &lt;num&gt; is a counter that starts at 0 and increases as needed. When there are no more comments to receive, the next page in the sequence will simply contain an empty string. For example, navigate to the page




<a href="https://imgur.com/user/LastAtlas/index/newest/page/0/hit.json?scrolling">http://imgur.com/user/LastAtlas/index/newest/page/0/hit.json?scrolling</a>




Now, increase the page counter in the address by 1. If we set the page counter to 100, for instance, we’ll see that the page is empty. However, there’s no way to know beforehand how many pages each user requires.




If the username does not exist or has not been used to post any comments, you may simply print a message and end the program. Otherwise, you should sort through the user’s comment data to find the top 5 comments (i.e. the comments with the most points). Your output should list these comments in descending order of points, detailing the post identifier (the “hash”), title of the post commented on, number of points received, and timestamp or the comment. In the case of a tie between points, break the tie by comparing “hash” values.




<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4724262e332b2e2907373e2a26242f2e2922">[email protected]</a>$ python imgur_info.py

Enter username: LastAtlas

<ol>

 <li>XJ7xbSk Points: 19</li>

</ol>

Title: This man pulled, pushed and lifted his disabled twin brother through an IronMan. Here is a touching picture of them at the finish line.

Date: 2014-08-24 15:36:54




<ol start="2">

 <li>wEF0R</li>

</ol>

Points: 11

Title: What a guy

Date: 2015-08-02 04:00:30




<ol start="3">

 <li>ZsqSJ</li>

</ol>

Points: 7

Title: MRW I find out I am unknowingly sharing a BF

Date: 2015-01-25 15:43:58




<ol start="4">

 <li>HfrBZSJ</li>

</ol>

Points: 5

Title: This is just magnificent Date: 2014-02-17 03:42:57




<ol start="5">

 <li>NLiuVXC</li>

</ol>

Points: 5 Title: My wife…

Date: 2014-02-17 09:58:07








