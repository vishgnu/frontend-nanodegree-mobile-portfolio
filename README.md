Changes for index.html:
===
* added caching (the IIS config is in the web.config file e.g appache will require correct module and .htaccess file)
* resize images
* make google analytics and perf.js load async and put to end of page
* disabled font link and inlined page style
* set media for print.css


For pagespeed testing the site can be opend from my azure instance running here
http://udacity2.vishgnu.org/
via 
https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fudacity2.vishgnu.org%2F&tab=mobile


Changes for pizza resize in main.js
===

* change all jqeury get for ids to  getElementById()
* removed size calculation completetly from size setting loop (pizzacontainers[i].style.width = newwidth;)
* calculate size based on first pizza reuse for all
* get looping parameters from already loaded list that need to be iterated later

Changes for 60FPS scrolling
===
1. updatePositions()
* removed calculation of sin values from looping of positionsetting (only 5 different values so they are precalulated)
* getting scrollTop value only once 
* change jquery to geElementsByClassname for .mover
*
2.addEventListener('DOMContentLoaded', function () 
* reduce number of pizzas to 50
* take jquery to get movingpizzas object out of looping to get only once and use for append


Misc
===
* changed pizzageneration loop (not relevant for resize but pageload)



