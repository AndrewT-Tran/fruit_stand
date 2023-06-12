Double-Charging Dojo Fruit Store
================================

**Learning Objectives:**

*   Practice using git (git clone)
*   Perform some basic logic on data from a POST request
*   Debug some common errors when implementing POST routes
*   Explain what statelessness is and its limitations
*   Reference static css or images
*   Make your key assignments/projects look better
*   Demonstrate how rendering HTML on a URL that received a POST is a bad idea

* * *


What We Know So Far
-------------------

So far we can do a few things in flask already:

*   We can collect data from the client using a form
*   We can use data from the server to render HTML pages with dynamic data
*   We can serve that HTML to the client to display the data

What if we want to collect data from the client, perform an action, like charging a credit card, and then show a confirmation page when the transaction is done? Technically we can do that too! However...

The Limits of Statelessness
---------------------------

With what we know now, we can't use the data collected from the user in another route on the server, because we have no way to persist data from route to route, or across successive HTTP requests. This is what is called _statelessness_.

In the next optional assignment you'll be building a project using what you know, and with no way to persist data from route to route. The intention of this assignment is to discover why this is a serious limitation, and why we will need to be able to persist data going forward.

Recognizing Design Flaws ~ Rendering on a POST
----------------------------------------------

![image](https://github.com/AndrewT-Tran/fruit_stand/assets/112746783/8a9a6523-7a20-4d5b-aa03-c01a1028930d)

Have you ever seen this pop-up window on a site? How did it affect your confidence in the site itself? During this assignment you'll be building a clickable prototype for an e-commerce application with what you know, and discover why it is poor design to render on a POST. For now, that's the best we can do.

_**IMPORTANT:** You do not need to solve for this design flaw in this assignment. We will address data persistence in the coming modules._

The Assignment
--------------

Start by cloning the repo found here: [https://github.com/mchoidojo/dojo\_fruit\_store](https://github.com/mchoidojo/dojo_fruit_store)

For this assignment, you'll be building a small web app as illustrated below:

![image](https://github.com/AndrewT-Tran/fruit_stand/assets/112746783/c919e373-2870-4a61-8b01-faf90e5db506)

Note that the template allows you to use simple if statements and for loops, but is not really a place to do much more than that. If you're wanting to do any calculations, you would want to do this in the routing file (server.py).

Also, remember that all form inputs are received as strings. If you want to work with them as numbers, use the int() method to convert a string to an integer. For example:
```
"1"+"2"+"3" \# returns 123
int("1")+int("2")+int("3") \# returns 6 copy
```
**Note for Mac Users:**

To get this code to run, you may have to add the following shebang to the top of your file to specify which version of Python to run on.
```
#!/usr/bin/env python3
```

You can read about shebangs and how they work [here](https://en.wikipedia.org/wiki/Shebang_(Unix)).

*   Display all the provided images of fruit on the fruits.html page
    
*   When the Checkout button is clicked, have the correct information display on the checkout.html page
    
*   In the checkout method, add a print statement to display in the terminal that says "Charging \[customer's name here\] for \[count\] fruits". For example, if the user's name is Sam and they ordered 5 fruits, the print statement would read: "Charging Sam for 5 fruits"
    
*   While on the checkout screen, hit the refresh button in your browser. Then check your terminal--what do you notice?
