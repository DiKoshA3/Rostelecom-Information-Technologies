<!-- PROJECT LOGO -->
<br />
<div id="header" align="center">
  <img src="https://s14.stc.yc.kpcdn.net/share/i/12/13143964/wr-960.webp" "Optional title"/>
</div>
  <h3 align="center">Rostelecom Information Technologies</h3>


<!-- ABOUT THE PROJECT -->
## About The Project


Testing the Rostelecom website: 
1)Login and password authorization:
-by login and password;
-by phone number, "Number" button;
-by phone number, "Mail" button;
-by phone number, "Login" button;
-by phone number, the "Personal account" button.
2) Authorization by time code.
3) Password recovery:
-type of password recovery;
-restore the client's password by phone number, the "By phone number" button;
-restore the client's password by phone number, the "By e-mail" button.
4) Registration:
-basic steps;
-with the setting (Block/Disable cookies).
Automated site testing https://b2c.passport.rt.ru 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

The following test design techniques were used when testing the site:

* boundary value analysis;
* division into equivalence classes;
* testing states and transitions.


The PyCharm libraries used in testing:

* requests
* python-dotenv
* pytest
* selenium
* faker

To start testing, you need to click "run".
A website was used to generate a temporary email address. www.1secmail.com

The project contains two folders __pages__ and __tests__, as well as files conftest.py and pytest.ini.

* conftest.py - a fixture for working with the browser.

* pytest.ini markers for parameterization.

The __pages__ folder contains the following files:

* registration_email.py - GET requests to a virtual mailbox to receive a valid email address and a code for registering on the website and password recovery;

* config.py - the main URL of the tested site;

* auth.py - wrapper functions for locators, distributed by classes depending on the subject of the tests;

* base.py - functions for applying explicit expectations to locators, getting the main page of the site and the path of the current page;

* locators.py - XPath and CSS locators of web site elements;

* settings.py - data used in the test process.

The __tests__ folder contains the following files:

* test_registr_positive - positive tests of the registration page;

* test_auth_page_positive - positive authorization page tests

**To restore the password, you must enter the captcha manually, as well as to verify password and email authorization.**



















