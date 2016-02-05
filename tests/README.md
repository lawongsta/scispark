Test scripts to check htmls
===========================

Required:
Python 2.7+
PhantomJS 

Python libs
* selenium
* pyvirtualdisplay
* tika
* reppy
* nltk

These checks cover:
* check for robots.txt file
* check for alt TEXT in img tags
* check for PDF text and download links where PDF links are given
* simple spell checker 
* check that images linked to exisits in the /image folder


To use
Run python htmlPageChecker.py -p <[htmlPage]>

e.g. python htmlPageChecker.py -p ../scispark-website/index.html
     python htmlPageChecker.py -p '../scispark-website/index.html, ../scispark-website/index.html'
     python htmlPageChecker.py -p scispark-website/*.html

If you wish check for robots.txt, please edit main() accordingly. 

Note that you can add words to filelist for spellchecking (specialDict.txt)

** I'm addressing an issue here. If you want run on site on the web, please use Firefox. For local files, use PhantomJS. 
Todo this change self.driver = webdriver.PhantomJS() to self.driver = webdriver.Firefox() and vice versa

TODOS
=====
* the browser issue
* better spell checking
* increase num of tests
* Handling for local or remote sites