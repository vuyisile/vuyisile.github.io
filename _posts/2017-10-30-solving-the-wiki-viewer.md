---
Layout  :
Title   : Solving the wiki viewer.
Date    : 2017-10-30
---

# The Wikipedia Viewer.


I just finished Free Code Camp’s Wikipedia Viewer app, where you generally pull random articles side-by-side from Wikipedia using the MediaWiki Web API,
the application also allows you to search for specific articles using the search box.

  
## Instructions:

-    Fulfill the below user stories. Use whichever libraries or APIs you need. Give it your own personal style.
-    User Story: I can search Wikipedia entries in a search box and see the resulting Wikipedia entries.
-    User Story: I can click a button to see a random Wikipedia entry.
-    Hint #1: Here's a URL you can use to get a random Wikipedia article: https://en.wikipedia.org/wiki/Special:Random.
-    Hint #2: Here's an entry on using Wikipedia's API: https://www.mediawiki.org/wiki/API:Main_page.
-    Hint #3: Use this link to experiment with Wikipedia's API.
-    Remember to use Read-Search-Ask if you get stuck.
-    When you are finished, click the "I've completed this challenge" button and include a link to your CodePen.
-    You can get feedback on your project by sharing it with your friends on Facebook.

## Logic:

Based on the instructions and the example given to us, the Wiki-Viewer is an API based project,
 so I create a function that pulls/gets random or specified articles. A better way to do this would is to separate the two problems,
 have a **get random article** function and a **get specific article** function.

## My Approach:

After completing the previous project (The Random Quote Machine), I had an idea or knowledge of **APIs, JSON and AJAX**,
-   First, I created a button for the **random article** that opens a new tab and displays any article from "https://en.wikipedia.org/wiki/Special:Random".
-   Secondly, understanding that this application is a search engine for Wikipedia, I created a html button and linked it to a function that **searches**  an article and used the **$.ajax()** 
    to pull requested data from this API "https://en.wikipedia.org/w/api.php?action=opensearch&format=json&limit=15&search= " +
    - I created **input** which is a variable that stores any thing that is currently entered in the **search box** (in the front end) and in the Back-End it is presented as:
      #### var input = document.getElementById("input").value;.
    - so whenever the user searches for anything the **search button** is there to send what is in the search box and add it to the url-API,
      which will look like this "https://en.wikipedia.org/w/api.php?action=opensearch&format=json&limit=15&search= " + **input**, and after $.ajax pulls request data is displayed on the window.