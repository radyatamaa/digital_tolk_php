# digital_tolk_php

Do at least ONE of the following tasks: refactor is mandatory. Write tests is optional, will be good bonus to see it. 
Please do not invest more than 2-4 hours on this.
Upload your results to a Github repo, for easier sharing and reviewing.

Thank you and good luck!



Code to refactor
=================
1) app/Http/Controllers/BookingController.php
2) app/Repository/BookingRepository.php

Code to write tests (optional)
=====================
3) App/Helpers/TeHelper.php method willExpireAt
4) App/Repository/UserRepository.php, method createOrUpdate


----------------------------

What I expect in your repo:

X. A readme with:   Your thoughts about the code. What makes it amazing code. Or what makes it ok code. Or what makes it terrible code. How would you have done it. Thoughts on formatting, structure, logic.. The more details that you can provide about the code (what's terrible about it or/and what is good about it) the easier for us to assess your coding style, mentality etc

And 

Y.  Refactor it if you feel it needs refactoring. The more love you put into it. The easier for us to asses your thoughts, code principles etc


IMPORTANT: Make two commits. First commit with original code. Second with your refactor so we can easily trace changes. 


NB: you do not need to set up the code on local and make the web app run. It will not run as its not a complete web app. This is purely to assess you thoughts about code, formatting, logic etc


===== So expected output is a GitHub link with either =====

1. Readme described above (point X above) + refactored code 
OR
2. Readme described above (point X above) + refactored core + a unit test of the code that we have sent
Thank you!

=================
Explained The Refactor Code
=================
The Weakness Old Code : 
1. There are no interface for implemented the function such as Repository, which are the codes doesn't be a clean for implemented
2. There are no Bussiness Logic Layer , bussineess logic the codes mostly implement the logic in Controller which are the code did not made a cleaned
3. The Repository didn't made a grouping base on logical goals, too much function handle on one repository (BookingRepository)
4. There are some functions have made doesn't be a clean code such as getAll(Repository) and etc. Have many if condition whereas the logic could make a simple if condition

What are changes The Code : 
1. Each the layer have an Interface such as Service Layer, Repository Layer. So the code make more be a clean and an interface we can mock later on Unit Test
2. Each Logic have a layer start from Repository Layer (for data query) -> Service Layer (for bussness logic) , Delivery Layer / Controller (for Endpoint API)
3. The Repository made a group in accordance logical goals
4. There are some function Optimized such as getAll(Repository) and etc.

What are adds The code : 
1. Added example unit test with mocking schema and with each the layer
2. Added Providers App service for Dependency injection Register Interface

