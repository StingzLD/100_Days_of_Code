# 100 Days Of Code - Log
**** Note: Any day that specifies "Day xx.5" refers to a day that was mainly full of research, and not so much coding. Since this challenge is to code for one hour a day, I would feel like I was cheating if I was to use those days as actually part of the challenge, even though there was still plenty of learning happening. Regardless, those days and related notes are still present in this log as a reminder of what all was learned and to show that progress was still being made, rather than there just being gaps in the log. ****

### Day 78: August 4, 2021

**Today's Progress**
* Completed Vmware SSH script.

**Thoughts**
* Just when you think you are done, there is always something else to add. Today, that something was verbose logging. I decided that creating just a basic log was not very useful, so I decided to make it fairly verbose for the type of script that it is. It provides the normal feedback that is provided to the console, as well as additional connection info to track who is actually logging into the servers and the full error details, should an error actually be present. The only other thing I may add is pulling the IP of the local machine it is run on and external IP of the network the machine lives on. That will provide plenty of details for auditing purposes, should the need ever arise.

**Link to work**
* [VMware PowerCLI Scripts](https://github.com/StingzLD/Powershell_Scripts/tree/master/VMware)

### Day 77: August 3, 2021

**Today's Progress**
* Started learning about [REST APIs](https://realpython.com/api-integration-in-python/).

**Thoughts**
* So far, REST APIs seem pretty straightforward. I have only really touched the basics, though, so we will see what the rest of this lesson has to offer. Up to this point, though, it has given me a pretty good understanding of how they work at the base level, which will be useful when working with/creating my own APIs.

**Link to work**
* [Real Python REST API Repo](https://github.com/StingzLD/Real_Python/tree/main/Python_and_REST_APIs)

### Day 76: August 2, 2021

**Today's Progress**
* Updated VMware SSH script.

**Thoughts**
* It seems there is almost always something else you can do to improve upon a script, and this was no exception. I decided to add some error handling to catch credential issues, set the script up with parameters, so certain user input prompts could be avoided, updated the code to utilize those new parameters, cleaned up some repeated code with functions, update some output color formatting, and found a missing piece of code that would have been a huge issue when running the script live instead of against my test output.

+ Overall, I am very happy with how far along the script has come, especially with how modular I have created. I already separated all of the core code out into a template file, so the only thing that needs to be touched are adding helper functions in, then using those in the two location functions. The only major piece of this script left to do, which I was not even thinking about until someone else brought it up, was to have it auto-log the output for auditing purposes. I started messing with it, but the file is not outputting everything I am seeing in the terminal, and making it do so takes away all visibility in the terminal, so I am going to have to find a way to balance all of that out tomorrow.

**Link to work**
* [VMware PowerCLI Scripts](https://github.com/StingzLD/Powershell_Scripts/tree/master/VMware)

### Day 75: August 1, 2021

**Today's Progress**
* Completed the Asymptotic Notation lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* After learning about algorithm time complexity in the MIT course, and taking a while to fully grasp the logarithmic part, it was nice to have this be my first lesson back on Codecademy. This allowed me to further practice the only part that I had trouble with in the class, which was definitely good for me. It looks like I might be seeing more of it in the near future, too, as the majority of the CS102 lessons that remain involve different algorithms.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 74: July 31, 2021

**Today's Progress**
* Completed the Final Exam of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* What a way to end a class! I pass my final exam with a 97%, leaving me with an overall grade of 99% for the entire class! I have to admit, though, that I am really peeved because two of the multiple choice questions on the final were actually wrong (I verified the answers from multiple sources, including the actual lecture slides, course study guide, and textbook, after submitting the exam). At the end of the day, those were only worth one point each, but it still really bugs me that it says I got them wrong, when I in fact did not. Nonetheless, I GOT A 99% ON MY FIRST MIT COURSE!!!!!! Super freaking exciting!!! I cannot wait until October for my next course to start!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%207%20-%20Plotting)

### Day 73: July 30, 2021

**Today's Progress**
* Completed VMware multi-location SSH script.

**Thoughts**
* Well, I have to admit. I did not think I was going to take this script as far as I did. Although the script was technically complete after only working on it for a little bit, it was not complete enough to my liking. In fact, even the single location was not super great, so I may go back and edit it later. Regardless, I certainly went all out with this script. It is full of error handling, console text formatting, and it is designed in such a way that I can reuse this script for literally anything I need to run against the VMware vCenter appliances. All that is needed to do so is to update the main functions with the necessary code, and it is ready to go. I have to say that I am fairly proud about this one. The only thing that would make it better is to set the location of the files as System Environment Variables (like how they are already being used for other private variables), scrape data from both our wiki and vCenter servers to ensure the locations lists are fully up to date, then provide an answer file to the user inputs in the script for full automation. Maybe I will play with that later to test it out.

**Link to work**
* [VMware PowerCLI Scripts](https://github.com/StingzLD/Powershell_Scripts/tree/master/VMware)

### Day 72: July 29, 2021

**Today's Progress**
* Updated Meraki firmware script.
* Completed VMware single location SSH script.

**Thoughts**
* There really is not much to talk about today, as I just continued working on the Meraki firmware script, as well as added a new VMware script to the mix for SSH. This basically takes the previous enable/disable SSH scripts I wrote and updated them to be all in one. I also put the commands inside of functions to be called. Although this really has no impact when running the script, as each function will only be ran once, I did this in preparation for the upcoming script that will use the same base code to run against multiple locations. I am still unsure exactly how that script is going to look, but I guess I will find our tomorrow.

**Link to work**
* [Private Meraki Repo](https://github.com/StingzLD/PSMeraki_Scripts)
* [VMware PowerCLI Scripts](https://github.com/StingzLD/Powershell_Scripts/tree/master/VMware)

### Day 71: July 28, 2021

**Today's Progress**
* Completed VMware SSH script.

**Thoughts**
* One of the immediate needs I saw at work was the ability to enable/disable SSH on all VMware hosts at a given location at anytime. Sure, you could manually go into every host's configuration and adjust it, but that would take forever, and I am all about automating as much as I possibly can. So what did I do? Naturally, I started down the automation road. The script itself went through a ton of iterations before the end of the day, and the result was something that I am fairly proud of, especially since we have a rather unique environment. My biggest concern with automation, as you could probably guess by now, is making scripts that are agnostic to the environment, so they can easily be reused wherever. This means not hard setting any variables to the environment, which also increases the security of the environment should the script be compromised. That being said, I am also a fan of not having to type in a bunch of variables every time I need to run a script, when I know that those values will never change for our environment. To solve this problem, I decided to do something a little unusual with my script, and that was to set System Environment Variables on the machine that will be running the code, then assigning those variables to variables used in the script. Of course, it is all documented within the script itself, but I thought this was a pretty clever way to get around the hard set variables in the script while also preventing more work for the user than is necessary.

**Link to work**
* [VMware PowerCLI Scripts](https://github.com/StingzLD/Powershell_Scripts/tree/master/VMware)

### Day 70: July 27, 2021

**Today's Progress**
* Continued Meraki API testing.

**Thoughts**
* Today was another successful day of playing with the Meraki API. Although I still have no actual script to show, my knowledge of various tools has grown immensely. By continuing with the Meraki API labs on the [Meraki DevNet](https://developer.cisco.com/meraki/) site, I was introduced to a few new tools that I have personally never used before like [Node.js](https://nodejs.org/en/), [Postman](https://www.postman.com/), [Docker](https://www.docker.com/), and [ngrok](https://ngrok.com/). Although I still have not touched most of them that much, I played around with Postman like crazy. It was so much, and I am going to be utilizing whenever I am playing with other APIs in the future. It is such a fantastic tool. Aside from all the playing, though, I did work on some more coding, which consisted of converting other scripts into a more universal format. I really like it when you can just plug and play snippets of code from one script to the next, as it makes the entire process so much easier. Like yesterday, though, everything is currently in a test state using private information, so changes have been made to the private repo.

**Link to work**
* [Private Meraki Repo](https://github.com/StingzLD/PSMeraki_Scripts)

### Day 69: July 26, 2021

**Today's Progress**
* Started Meraki firmware script.

**Thoughts**
* One of my current goals at work is to automate a lot of Meraki configurations, whether it be for new installs or changes. I was given another task to create a firmware script, and I was handed another PowerShell script using the PSMeraki module that someone had started but did not get very far into. Before proceeding, I decided to check out the [Meraki DevNet](https://developer.cisco.com/meraki/) site to see what I could leverage in the API, since I will be doing a lot more with automating these processes. To my surprise, they are not using this PS module at all. Instead, their API is based entirely on their Python SDK. Nice! This is super exciting for me because, as you know, that is the exact language I am trying to master right now. Could this opportunity have been any better?! Needless to say, I spent a lot of time of going through their modules, then playing around with the API to try a bunch of different stuff out. Since my test scripts are using private information, you will not be able to see what I have been playing around with. However, once I have official builds out (the scripts will be agnostic), they will be posted to a public repo.

**Link to work**
* [Private Meraki Repo](https://github.com/StingzLD/PSMeraki_Scripts)

### Day 68: July 25, 2021

**Today's Progress**
* Further explored logarithmic time complexity.

**Thoughts**
* Although there was not actually any code written today, I feel like what I have learned today was beneficial enough to count towards a day of coding, unlike previous days where I spent it only researching. Why? Mainly because it was not just going through the motions. I was determined like crazy to fully understand logarithmic time complexity, and I absolutely succeeded today! So what was it that finally made this topic click for me? Relearning a math concept that I originally learned all the way back in middle school: the logarithm.
  
  Mind you, I have not taken any math course in over 15 years, so even parts of Algebra II have faded into the abyss by now. For this, I ended up on [Khan Academy](https://www.khanacademy.org/math/algebra2-2018/exponential-and-logarithmic-functions/introduction-to-logarithms/a/intro-to-logarithms), which did a fantastic job of walking through everything and testing your knowledge. With that knowledge fresh in my mind, I continued looking for that holy grail explanation, and I found it a few comments down in this [Stack Overflow](https://stackoverflow.com/questions/2307283/what-does-olog-n-mean-exactly) post. Specifically, it was [this image](https://i.stack.imgur.com/spHFh.png) that really brought everything home. It was not so much the binary tree in the image, as I have seen lots of those when describing the logarithmic time complexity, but it was the explanation below it describing what the tree looked like as an equation that finally made me go "AHA!!!"
  
  This combined knowledge of logarithms with the binary tree equation was exactly the explanation I was trying to find to make it all click. I cannot tell you how relieved I am to finally fully understand why the logarithmic time complexity is the way it is.

**Link to work**
* None

### Day 67: July 24, 2021

**Today's Progress**
* Started additional research into time complexity.
* Turned into working on search algorithms.

**Thoughts**
* TL;DR Went to dive deeper into time complexity, but instead dove head first into the rocky coast of Binary Search Algorithms. Time complexity research will continue tomorrow.

+ Phew! What a day. I had started researching more about time complexity, and then I discovered a lesson about it on [freeCodeCamp](https://www.freecodecamp.org/news/time-complexity-of-algorithms/). Towards the beginning of the lesson, they give links to two tutorials on HackerEarth about [Linear Search](https://www.hackerearth.com/practice/algorithms/searching/linear-search/tutorial/) and [Binary Search](https://www.hackerearth.com/practice/algorithms/searching/binary-search/tutorial/), which I decided to go ahead and do, even though I had already written code for those in the MIT course. This led to a very, very long session of confusion and perseverance.
  <br><br>
  The Linear Search challenge was nice and easy, that is after I figured out how in the heck to work with their system. At first, I thought you just hard set the sample numbers into your code, then run it accordingly. Well, that turned out to be highly incorrect. Even though hitting the "Compile & Test" button passed because of having the proper values hard set, it turns out there are additional tests that happen once you hit "Submit". Now I was stumped on how I was actually supposed to put all these test values in, and unfortunately there are not a lot of tutorials out there on how to actually use this system. I eventually figured out each line in the input is actually a separate input, as if a user was entering each line when prompted to do so. Once I had that figured out, I passed every test for this tutorial.
  <br><br>
  The Binary Search challenge, on the other hand, was incredibly brutal. Instead of referring back to previous lesson notes and code, I wanted to do this from complete scratch, which turned out to be fairly interesting considering it has been a few weeks since the lesson. Normally when dealing with these in the classroom setting or tutorials, you just have a list of numbers already sorted and ready to go, or you have specific low and high values given to you to use for generating your own list. In this case, you have every value given to you via inputs, which are strings. This means you have to convert everything accordingly, which led to researching how to properly take a string of numbers and convert them into a list without having to write a separate function (after all, the goal is efficient time complexity). Needless to say, I was not expecting to have to map the split input into integers while also using list on the whole thing. Once that tested successfully, I then ran into issues with how I was actually writing the search code. Testing the sample input would work great, up until I hit the final element in the list. This led to me debugging like crazy, including walking through everything via pencil and paper, drawing visuals to fully comprehend the entire process. After spending way too much time on it, I finally figured out what I was doing wrong, although the solution did not make any sense to me at first. It was not until I went back to the pencil and paper with the solution to test it that I realized how it would work without rasising an error.
  <br><br>
  Although this was a great learning experience for the binary searching algorithm, it literally had zero effect on me getting closer to fully comprehending time complexity. I am very persistent (read stubborn), though, so my research shall continue tomorrow for the holy grail of time complexity explanations.

**Link to work**
* [HackerEarth Repo](https://github.com/StingzLD/HackerEarth)

### Day 66: July 23, 2021

**Today's Progress**
* Completed the Meraki Syslog Server Script.

**Thoughts**
* Today I took a bit of a tangent to work on some scripting for work. What started out as just helping someone with a script turned into a full day of coding. We are venturing into automating our Meraki deployments, and to do so we are utilizing a PowerShell module called [PSMeraki](https://github.com/sanderkl/PSMeraki). Having never touched this before, I had a lot of learning ahead of me, but I was not anticipating on fixing the module itself. While writing the script, I kept running into issues with functions that were supposed to be public not being found. Eventually, I found out why, and after applying the fix locally, brought the issue up on the module's GitHub page. That led to me creating my own fork of the repo, so I could submit the changes in my first ever Pull Request (I have been on the receiving side before, but never on the submitting side). Once I got that resolved, I was able to complete the script, which went through many, many iterations of more and more efficient code. Unfortunately, I did not make a repo before I started the work, but that was mainly due to the fact that I was testing the script with hard set values that should remain private. It would have been bad news if I accidentally put that information out there publicly! Regardless, the final script is live, and I cannot wait to start working on the rest of the automation scripts.

**Link to work**
* [Meraki Syslog Server Script](https://github.com/StingzLD/Powershell_Scripts/blob/master/PSMeraki/setSyslogServers.ps1)
* [My Forked PSMeraki Repo](https://github.com/StingzLD/PSMeraki/tree/psd-patch-1)

### Day 65: July 22, 2021

**Today's Progress**
* Completed Lecture 13 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This was a pretty cool lecture, as it was all about plotting. I did end up using matplotlib instead of pyplab, though, as pylab is not really a great tool or used very widely because of that fact. This is definitely an introduction into using these tools, though, as it did not go very in depth. My guess is because we will go deeper with it in the second course, as this is the last lecture of this course!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%207%20-%20Plotting)

### Day 64: July 21, 2021

**Today's Progress**
* Completed Problem Set 6 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* I am left feeling very conflicted about having completed the last problem set of the course. On the one hand, it is nice to finally be done with this unit because it was by far the hardest part of anything I have learned in programming up to this point. And I mean everything, not just the hardest part of this class. On the other hand, I still do not fully grasp algorithmic complexity, as was evident by this problem set. This is the only problem or exercise set that I did not get a 100% on (got 89%), and that is because something is still not clicking. I even asked my best friend for clarification, who is back in school and just went through all of this. Unfortunately, he is just as confused as I am about it. I then decided to ask my other friend who has been a professional developer for years now (specifically Python), and even he is admitting that he does not fully grasp it. Sure, I feel better that I am not alone in this, but this feeling is something that eats at me, and it is one of the worst feelings in the world to have. The one thing I detest more than anything in the world is not knowing how to do something, especially when that something was taught to you in a classroom setting. You can guarantee that I will absolutely be continuing my research on this topic between now and the final exam.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%206%20-%20Algorithmic%20Complexity)

### Day 63: July 20, 2021

**Today's Progress**
* Completed Lecture 12 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This lecture was slightly easier than the last, but only because it had less to do with figuring out the exact type of complexity and more on comparing different styles of sorting algorithms. Looking at two functions and figuring out which is going to be more efficient is relatively easy for me, but for some reason the Big-O notation is just not clicking. We shall see how the final problem set for this course turns out.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%206%20-%20Algorithmic%20Complexity)

### Day 62: July 19, 2021

**Today's Progress**
* Started Lecture 12 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Between the last lecture being so intense, finishing my first week at a new company, and having a lot of work to do at home, I decided to take the weekend off from programming to keep myself from burning out. Continuing with my classwork, I started Lecture 12. So far, this has basically been an extension of the previous lecture, while at the same time diving deeper into searching and sorting algorithms. There is still some reference to complexity, as introduced in the previous lecture, but it is nowhere near as in depth. Nonetheless, I will still be continuing my research on complexity after the class has finished.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%206%20-%20Algorithmic%20Complexity)

### Day 61: July 16, 2021

**Today's Progress**
* Completed Lecture 11 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Holy moly, guacamole. This was BY FAR the hardest lecture. In fact, this is the only one that I still do not fully comprehend, even though I was able to answer the exercise questions correctly. This is also the only topic that I have had to research for a while, but something is still not clicking. Sure, I can put two and two together, and I can tell you what each Big-O value goes to what, but I am the kind of person that really likes to understand why something is the way it is, not just take it at face value. It is this level of understanding that has me completely confused right now, and I will definitely need to spend some more time, outside of the class and this challenge, researching to get my answer.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%206%20-%20Algorithmic%20Complexity)

### Day 60: July 15, 2021

**Today's Progress**
* Completed Problem Set 5 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).
* Started Lecture 11 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* I should have just completed the problem set yesterday, as the final assignment was literally five lines of code, but c'est la vie. That just means I got to start Unit 6 earlier than anticipated! Lecture 11 is about computational complexity and making your programs efficient. This goes back to the topic I admittedly kind of glazed over on Codecademy, but it looks like I need to pull in the reigns and truly learn this.

**Link to work**
* [Private Repo for Classwork (Problem Set 5)](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%205%20-%20Object%20Oriented%20Programming)
* [Private Repo for Classwork (Lecture 11)](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%206%20-%20Algorithmic%20Complexity)

### Day 59: July 14, 2021

**Today's Progress**
* Continued Problem Set 5 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Today, I was able to complete Parts 2 & 3 of the problem set, which entailed creating the new PlaintextMessage class, as well as the CiphertextMessage class. Both of these were subclasses of the Message class, with the former encrypting the message and the latter decrypting a message using multiple ciphers via brute force. Tomorrow will be the final piece of this problem set, then comes the final unit of the class!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%205%20-%20Object%20Oriented%20Programming)

### Day 58: July 13, 2021

**Today's Progress**
* Started Problem Set 5 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Problem Set 5 consists of encrypting/decrypting a message using the Caesar Cipher. To do this,  we are to write a series of classes and methods to perform these operations. Now, I have already done a Caesar Cipher challenge before, so I know roughly how I want to code this, however I have never done it with classes. While defining the first class, it was clear how different an approach this really is compared to just writing and calling functions. It will be interesting to compare the two sets of code side-by-side when I am done with this to see just how similar and different they truly are.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%205%20-%20Object%20Oriented%20Programming)

### Day 57: July 12, 2021

**Today's Progress**
* Completed Lecture 10 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This lecture continued down the OOP road by creating an entire hierarchy of classes that used other classes inside of them, which needless to say became very involved. The exercises that followed certainly caused you to think critically to fully understand what was being asked of you and how to properly implement it. Then once those were done, generators came into the mix, and creating what I thought would be a simple prime number generator turned out to be much harder to conceptualize than I was originally thinking. Of course, it would have been much easier if I had known about for/else before I started working on the assignment, but seeing as I had no idea that a for loop could have an else block, the possibility of using it was non-existent in my mind. But alas, I know about it now, and I will certainly remember that trick for future projects.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%205%20-%20Object%20Oriented%20Programming)

### Day 56: July 11, 2021

**Today's Progress**
* Completed Lecture 9 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This lecture's exercises were definitely the most challenging of them all, up to this point. I had never known about OOP up until a few months ago, back when I initially learned about classes through Codecademy. This style of programming is far different than my embedded programming experience, and it is still something I have to force my mindset into, as it does not come naturally to me yet. There are certainly parts of it where I can code through it without thinking twice, but the more complicated methods and interacting with other classes still feels like I am missing that one "AH HAH!!!" moment to make it all click. I am hoping that this moment will reveal itself between the next lecture and the problem set for this unit. We shall see!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%205%20-%20Object%20Oriented%20Programming)

### Day 55: July 10, 2021

**Today's Progress**
* Completed Problem Set 4 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Part B of Problem Set 4 ran much smoother than Part A, mostly due to there not being a problematic test file running against my code like last time. This part introduced a computer AI to the game, which was pretty fun, especially considering I wanted to add an AI element to the terminal game I created earlier in this challenge. Overall, though, I had a blast with this project. It was unique in that it was not just having you write code to make a game work, but it was designed to force you to write the code a specific way in order for it to work as intended. This made me rewrite what I was doing a few times before I finally got it nailed down, but it also expanded my capabilities and thought process on how to better resolve these issues in the future.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%204%20-%20Good%20Programming%20Practices)

### Day 54: July 9, 2021

**Today's Progress**
* Continued Problem Set 4 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Part A of this problem set was... problematic, to say the least. My code was running just fine on its own, however the test file that we were to run against the code had an issue. I was testing my code every step of the way, running both the script itself and the test against it as I went. All I needed was to add a single line of code to finish a certain function, but no matter how I wrote it (I tried four different ways), it always errored out when running the test, even though the script always ran fine by itself. Eventually I decided to run the function in Python Tutor, and it worked no problem. I then just input into the autograder to see what would happen, and it said it was correct. That means the test file that was written was messed up, and I was chasing down a problem for over an hour that never even existed. Silver lining is I now know multiple ways to write that one line of code!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%204%20-%20Good%20Programming%20Practices)

### Day 53: July 8, 2021

**Today's Progress**
* Started Problem Set 4 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).
* Started developing a PyCharm theme.

**Thoughts**
* Problem Set 4 is another game that I have to build, only this time it is a Scrabble/Word with Friends type game. The instructions for this game are much more in depth than the hangman style game, so I am definitely going to be spending a little bit of time creating and testing all of these functions.
* Going off on a little tangent, I decided to start using PyCharm with this project instead of Spyder, as I know programming via PyCharm is a highly sought after skill. I have to say, though, that right off the bat, I am not impressed. I find the interface to be not very user-friendly. For example, the Python Console is completely useless if you dock it on the right side of the program instead of on the bottom (default), but having it below the editor tab cuts off where you are coding, so it's kind of a no-win solution there. The default theme is really not pleasing at all, so writing code in this program does not make me feel happy in the slightest. Because of this, I ended up trying a bunch of pre-made themes, but most of them were either way too far out there (your eyes would hate you after only ten minutes of coding with them) or they just had font colors that were too conflicting (the part you need to focus on is not what your eyes are drawn to, so you are constantly forcing your eyes to focus elsewhere, which will end up in a migraine in no time). So what is the solution? Create my own theme! Sadly, this is much easier said than done. I wish it was as simple as just editing a JSON that already lives on your machine, but alas, it is not. Besides, I need a theme that I can use across all my devices, and the only way to do that is to create an official one and place it on the marketplace. Needless to say, I went down a huge rabbit hole of installing packages, plugins, cloning a template repo, modifying lots of files, and I am still barely started. Needless to say, this will be a project in itself, but it will awesome when it is finished!

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%204%20-%20Good%20Programming%20Practices)
* [PyCharm Theme Repo](https://github.com/StingzLD/PyCharm_Spyder_Theme)

### Day 52: July 7, 2021

**Today's Progress**
* Completed Lecture 8 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* For me, personally, this has been the most beneficial lecture of the entire course up to this point. I already knew about error handling, as I have implemented that in previous projects, however I never even thought to use it as a control flow mechanism in such a way as the course did. For example, I always simply used it as a "This error happened, now do/retry this", not a "I am going to write my code specifically so when a common and expected error pops up, i.e. a missing field in a list of lists, it will manipulate the data accordingly and continue processing everything else." It is a completely different way of thinking about error handling, and I am super excited about trying it out on my own projects. Between that and learning about assertions, I now have a whole new section added to my playbook.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%204%20-%20Good%20Programming%20Practices)

### Day 51: July 6, 2021

**Today's Progress**
* Completed Lecture 7 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This Lecture is all about testing and debugging, and it was very insightful. I already knew a fair amount about it, as I have done it in the past with embedded programming, but this went more in depth on the conceptual side of things. I will certainly be keeping what I learned in mind, as I move forward with writing code.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%204%20-%20Good%20Programming%20Practices)

### Day 50: July 5, 2021

**Today's Progress**
* Completed the Midterm of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* There were definitely some good challenges in the Midterm, although my biggest challenge was battling with the autograder. It had me trying to figure out what I was doing wrong on my last question because it kept saying it was incorrect, even though I tested it like crazy in my IDE before submitting. I eventually figured out that my debugging print statement was what was actually causing the issue, not the actual code or the result of the code, so I was chasing a problem with my code that didn't even exist. That being said, it did allow me to come up with multiple ways to solve the same problem, so it was still beneficial in the long run.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Midterm)

### Day 49.5: June 24, 2021 - July 4, 2021

This was an incredibly busy week and a half between the wife being out of town for a week (solo parenting is so much fun), job interviews and landing a new job (YAY!), and studying for the MIT midterm. Even so, I was still learning more about Python, just not doing much in the way of practicing coding. One topic I was heavily invested in was [Advanced Computer Vision](https://youtu.be/01sAkU_NvOY) using Python and [MediaPipe](https://google.github.io/mediapipe/) to track your hand, face, and body via your computer's camera. This is going to be super fun to start coding!

### Day 49: June 23, 2021

**Today's Progress**
* Completed Sandbox Problem Set 1 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This Problem Set was very reminiscent of a Problem Set from a previous Unit. It was still good practice completing the problems, though, as the only way to solidify a concept is to continue practicing it.
* I also ended up diving more into CircuitPython libraries and documentation, however I was only messing around by manipulating demo code, so I do not feel like that is worthy enough to be put into a separate repo, as the code was 99% not my own.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Sandbox)

### Day 48: June 22, 2021

**Today's Progress**
* Revamped the 808 Drum Machine.

**Thoughts**
* The 808 Drum Machine from the class was fun, but it definitely had some issues. The capacitive touch pads were way too sensitive, so much so that some of the sounds activated constantly without even touching the fruit, and it was not very visually appealing. After doing some research, I was able to find a way to light up the pixels without the use of the CPX module (it had a conflict with another module that was already coded), and I was able to find a way to calibrate the sensors using the touchio library that I was already using. After reworking the code, I was able to have a very fun drum machine. I even decided to take a video of it and put it up on YouTube (link in the repo).

**Link to work**
* [808 Drum Machine Repo](https://github.com/StingzLD/808_Drum_Machine)

### Day 47: June 21, 2021

**Today's Progress**
* Completed the entire [Learn Hardware Programming with CircuitPython](https://www.codecademy.com/learn/learn-circuitpython).

**Thoughts**
* Today, I decided to go on a little tangent. My programming background is mostly embedded programming, and I was working on some robotics with the kids over the weekend, but I wanted to use Python to program the electronics. Since I already have a Circuit Playground Express (I have only ever programmed it using MakeCode), and Codecademy has a course on CircuitPython, I figured this was a great way to use my current Python knowledge for embedded programming. Although the course was fairly simplistic and quick, as well as buggy, I was able to learn the basics of what I needed to in order to progress further with my own projects. Overall, it was a lot of fun, and the drum machine project at the end was a huge hit with the kiddos.

**Link to work**
* [CircuitPython Repo](https://github.com/StingzLD/Codecademy/tree/master/CircuitPython)

### Day 46: June 20, 2021

**Today's Progress**
* Completed Problem Set 3 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* This Problem Set was a ton of fun. It was creating a hangman game, which ultimately was pretty easy. However, it became far more difficult once we were challenged to rewrite all of the functions as one liners, some of them in more than one way. It was definitely hard because they hinted at what functions they wanted you to use, only we had never used or even heard of those before. The challenge then transformed into researching what the functions were, how to use them, then combining those with other aspects learned throughout the course to generate the one line versions. I definitely scratched my head more than a few times, but once I realized exactly what was going on, it was pretty straightforward.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%203%20-%20Structured%20Types)

### Day 45: June 19, 2021

**Today's Progress**
* Completed Lecture 6 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* As with Lecture 5, Lecture 6 went more in depth with Dictionaries than I have been before. We also went back and made previous exercises more efficient by utilizing dictionaries (e.g., calculating the Fibonnaci value of a number). It is amazing the difference in operations, and consequently speed, between the two programs.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%203%20-%20Structured%20Types)

### Day 44: June 18, 2021

**Today's Progress**
* Completed Lecture 5 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Lecture 5 had a lot of good information in, especially when it comes to mutability. That is one thing that had been mentioned in passing in some other course I took, but it was only to say something along the lines of "Immutable objects cannot be changed, whereas mutable objects can." Well, that is fairly bland, but at the time, I did not think there was really any more to it than that. Boy was I wrong. I mean, yes, that is ultimately what it means, but what that does not detail is just how important that can be. The biggest part of this is how the objects are stored/referenced in memory, especially when setting variables based on other variables, and knowing that how they each behave is completely eye-opening.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%203%20-%20Structured%20Types)

### Day 43: June 17, 2021

**Today's Progress**
* Completed Problem Set 2 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Admittedly, I had a decent amount of trouble working through the last problem of this set. In the end, it was mainly my brain just trying to overcomplicate the entire problem, but it did make for a good lesson in just walking away, taking a small break, then coming back to reevaluate the problem. After doing so, I realized I could have made my code a more efficient in the previous problems, from which this code was built upon, by solving the problems a different way. By reworking the previous problems' code, I was no longer trying to make inefficient code work, which allowed me to more easily picture the solution for the final problem.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%202%20-%20Simple%20Programs)

### Day 42: June 16, 2021

**Today's Progress**
* Completed Lecture 4 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* As mentioned before, this course is definitely taking what I learned to the next level, and I love it. I do believe that learning the basics of the language prior to taking the class has helped immensely, as it is certainly much faster paced than Codecademy was. What is great is that I am now just barely ahead in my learning on Codecademy than where I am on MIT, so it the concepts are still fresh in my mind, and I can just build on it with the MIT course. For example, we just finished learning about recursion in the MIT course, and I was able to push my ability to think in that manner with its more challenging exercises.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%202%20-%20Simple%20Programs)

### Day 41: June 15, 2021

**Today's Progress**
* Completed the Recursion Code Challenges and stared the Asymptotic Notation lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* As expected, the Recursion Code Challenges were not much different than the actual exercises, but that is okay. It was more practice, and the more you practice, the more familiar you will be with it.
* Asymptotic Notation is something that will be pretty useful in the actual designing of programs, and it is something that I have never really taken into consideration with other programming I have done, including robotics. I have always had programs that ran fast enough to where there was no noticeable lag in them, so it was never something I really thought about. The only limitation I have ever really come up against was creating code that would fit onto a certain chip, so efficient code was still necessary, but it was a different kind of efficiency: size, not operations.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 40: June 14, 2021

**Today's Progress**
* Completed the final set of Recursion exercises and quizzes in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Recursion is starting to grow on me, even though I still only see a limited use for it. I am hoping the upcoming Code Challenge for Recursion will actually be a challenge (the previous challenges were not much more difficult than the actual lessons).

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 39: June 13, 2021

**Today's Progress**
* Completed the first set of Recursion exercises and quizzes in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* I am still on the fence about Recursion, but after reading more about it on [Real Python](https://realpython.com/python-recursion/), I am starting to see how it could be useful in specific situations. It still seems to have a limited use, but it is good to know for those times where it can prove beneficial.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 38: June 12, 2021

**Today's Progress**
* Started Lecture 4 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* I am thoroughly enjoying this class so far. Sure, it is basically going over the same fundamentals of Python that I learned elsewhere, however the focus is not actually the coding itself. The focus is on the actual concepts behind what you are trying to write code for. Instead of "Let's go code XYZ, while I give a general overview of what you are doing means", the class is saying "Here is the problem we want to solve, here are some conceptual ways we could go about it, here is a way we can code this using Python, but what does it actually mean? What could we do differently to change the outcome? Why would that work?" It is definitely hitting all the Computer Science points that I was hoping it would, and since it is MIT, I would expect no less.

  Now, this isn't to say that how I learned the language initially was bad. The platform I used/still use (Codecademy) utilizes a very hands on approach to learning a language. However, it definitely holds your hand through the entire process, and although that can be helpful at times, I feel like it does more harm than good. The first time I learned Python a few years ago, I hardly retained anything at all. Once the course was done, I still couldn't code anything because I didn't really understand how to go about doing it. Sure, I could tell you what the actual syntax was, but that doesn't help much if you are having issues creating it from scratch. In fact, even going through the new Python 3 course years later, I still had issues retaining the information because it is very much a "Step 1: Do this. Step 2: Do this." process, and it leaves all the problem solving at the door. But that is where we learn the most. Being challenged and getting things wrong the first time, trying to figure out why it was wrong, then fixing those issues is the best way to learn. With the MIT course, it is very much about learning the core concepts of how and why everything works before code even gets involved. This is highly beneficial to me. Maybe it is because I already know the language well enough to do the basics without looking anything up, but even with that being the case, learning the how and why is what will allow me to take ideas from my head and put them into code.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%202%20-%20Simple%20Programs)

### Day 37: June 11, 2021

**Today's Progress**
* Completed Lecture 3 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Now we are starting to get deeper into concepts like algorithms and the math behind floats. This is what I have been looking forward to, and I am glad it is happening early on in the course. I am super excited to see how deep this rabbit hole goes.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%202%20-%20Simple%20Programs)

### Day 36.5: June 4-10, 2021

I decided to lump all these days into one half day entry, as there was not any actual coding happening. Instead, I was going through a new Python book that I had ordered from Real Python. This was actually quite beneficial, as the book went deeper into topics than my lessons had. I only barely scratched the surface of the book, but I know it will definitely be a good reference if I have any questions about how something works.

### Day 36: June 3, 2021

**Today's Progress**
* Completed Lecture 2 and Problem Set 1 of the [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/).

**Thoughts**
* Although the class is teaching parts of Python that I already know, the actual Computer Science behind the coding is being explained in much greater detail in this course. The textbook recommended for this course is a great resource for all kinds of Computer Science goodness. All that is left for Unit 1 is to complete the unit's Problem Set, which accounts for 40% of my grade.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%201%20-%20Python%20Basics)

### Day 35: June 2, 2021

**Today's Progress**
* Started [MIT Course 6.00.1x](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/), completing all of Lecture 1's assignments.
* Started the Recursion lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* As if I was not already challenging myself enough, I have officially started MIT course 6.00.1x: Introduction to Computer Science and Programming in Python. One bonus is that everything I have learned so far is pretty much going to be reiterated throughout this course, so it will be nice to have concepts that I already know in the class, while at the same time pushing beyond the limits of Codecademy's education. This is MIT, afterall, and it has already proven that it is going to make me think well outside the box. Its emphasis on Computer Science is really what is going to push my coding to the next level, and I cannot wait.
* Even though I spent today in the class, I still felt the need to progress at least a little in my Computer Science studies at Codecademy. Continuing on, I started learning about Recursion. This is another topic that I am very unclear on in regards to how it is actually going to be useful in the real world. Computationally, it is slower than iterating through a list because of its additional overhead, and I currently see no benefit of why I would not just use a list. There is clearly a missing piece to this puzzle, otherwise why would I be learning about recursion, linked lists, etc. if they were truly not any better than just using a list? I assume that is the downside to platforms like Codecademy who are simply teaching concepts, but only dive so deep. Luckily, I have the MIT course to take what I am learning at Codecademy to the next level.

**Link to work**
* [Private Repo for Classwork](https://github.com/StingzLD/MITx/tree/main/6.00.1x/Unit%201%20-%20Python%20Basics)
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 34: June 1, 2021

**Today's Progress**
* Completed the Hash Maps lessons and project in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Learning about and coding Hash Maps is the first time in this series of lists where I actually feel like I could benefit from using it in comparison to just a normal list, dictionary, etc. I cannot think of a good example of how I would utilize it off the top of my head, but hashing in general is a concept I am very familiar with because of my IT background, and utilizing that for indexing a database to find items quicker than iterating than huge lists just makes sense to me. We shall see how much deeper we go with these during the course, or if we are moving on altogether, but I would like to keep using these to get more comfortable with coding them.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 33: May 31, 2021

**Today's Progress**
* Continued the Hash Maps lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Today involved a lot of conceptual learning about Hash Maps and the different methods of creating them. On the coding side, I was only able to complete the creation of the HashMap class today, but with the conceptual part out of the way, tomorrow's learning should be mostly about coding.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 32: May 30, 2021

**Today's Progress**
* Completed the Stacks project and started the Hash Maps lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Completing the rest of the Stacks project (Towers od Hanoi game) really made me think about my Python Terminal Game (Connect Four) and how I could have coded it differently to utilize OOP. I may end up going back and rewriting it using OOP, but if I do that, then I will also want to introduce the AI to the mix. This sounds like a good use for a Dev branch of the repo. This will have to be done in free time, though, so it may be a while before I get to it, as I start my MIT Introduction to Computer Science class on Wednesday.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 31: May 29, 2021

**Today's Progress**
* Started the Stacks lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Today I learned about Stacks, which are pretty straightforward. I still do not see the benefit over just using a normal list (see notes from yesterday), but I am having no issues working with them so far. I am currently about halfway done completing the Towers of Hanoi project.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 30: May 28, 2021

**Today's Progress**
* Finished the Queues lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Queues are definitely a good example of using a single linked list, however I am still failing to see the benefit of all the extra work required to create, link, and remove nodes when you can easily make a queue with a standard list, add to the queue with the built-in append function, you don't have to link anything because lists are automatically indexed, and removal of the first item in the list can be done with the built-in pop or del functions. You also don't have to create methods for specific things like checking the size of the queue because you already have the built-in len function you can use on the list or peeking at the first item because you can just get the value of the first index by calling it. There must be some reason why linked lists are valuable, however, since there is a lot of focus on them in this course. I am sure the reason is I am not seeing it is because these queues are very basic to teach them, so perhaps I just need to go search for a more complicated queue to see the real benefit of them.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 29: May 27, 2021

**Today's Progress**
* Finished the Double Linked Lists lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).
* Cleaned up the CS101 Final Project.

**Thoughts**
* After finishing the lessons for Double Linked Lists, I can see a few real world use cases for them. In looking at the syllabus, I am very curious to see how all of this gets integrated into the upcoming lessons.
* I received some feedback on my terminal game in regards to PEP 8, so I went through and started cleaning the code up. This was mainly in regards to lines between functions and the spaces in my new_grid function, but also some tiny ones like using "is not None" vs using an equality operator like "!= None". I had no idea the latter was not really the correct way of doing that, even though the code worked just fine. I also decided to change some of the variables inside of the functions that shadowed global variables, even though you could still follow the code in the functions with ease. In doing all of this, I discovered linting using PyLint, and that was very nice to stumble upon. When playing with that, I also realized that these colored blocks that appear next to my code were actually clickable! That was a very handy thing to learn, and I will absolutely be making use of those in the future. Between all these little changes I have been making over the past week, I can comfortably say that code is now looking really nice. There are still some changes that could be made, but those changes would completely change the main structure and resulting in rewriting a lot of the program. It is probably best to just leave it as is, then introduce those types of changes on the next project.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 28: May 26, 2021

**Today's Progress**
* Started the Double Linked Lists lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* Okay, now we are getting somewhere with these types of lists. A regular Linked List did not make very much sense to me from a practicality standpoint, as with my current knowledge, I cannot foresee any use for such a list over just a normal list. Double Linked Lists, however, seem very useful to me. I was only able to complete about two-thirds of the lessons today, but I did enjoy these much more than just a single linked list. Being able to easily navigate both forwards and backwards in the list is a huge plus. Sure, there is a little more overhead in terms of reconstructing the node links when adding/removing a node, but that overhead is all done in the methods themselves, greatly outweighing any of the tediousness of navigating through a regular Linked List.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 27: May 25, 2021

**Today's Progress**
* Reworked the CS101 Final Project.
* Finished the Linked Lists lessons in CS102 of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* What I love so much about programming is constant learning of new ways to implement ideas. In this instance, I am talking about the use of f-strings. Now, I already learned that you could use an f-string to use variables directly in your strings, however I did not know you could do even more than that! My friend looked over the code said I should implement f-strings, and I was like "I already did where I could!". Enter the learning. Wow, I did not know you could use it to input practically anything! This is a total game changer. Between that and cleaning up some of the more repetitive things in the script, I can comfortably say that this game's script is looking pretty good now! I know I need to do something about the repetitiveness in the diagonal win checks, but I will have to spend some time thinking about how to do that, since it involves changes in the operators.
* Although I am still in the same boat as I was yesterday about linked lists (not exactly sure how these are helpful yet, in comparison to just normal lists), I did learn a bit about how to manipulate the lists to get some basic info out of them. I know there is still a lot to learn about these, so I am sure I will figure out the benefits of them soon enough. For now, I will just keep on trucking and soaking up all the information I can, so I will be fully ready once I do understand the benefits of using them.

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 26: May 24, 2021

**Today's Progress**
* Started the CS102 course of the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* I am very excited to be starting the CS102 course, as this course is all about Data Structures and Algorithms. This will certainly push my data handling, as well as programming, abilities to the next level. Today was learning about and coding Nodes and Linked Lists. I am still not exactly sure how this is necessarily helpful compared to a normal list, but I am sure I will find out soon enough.

**Link to work**
* [CS102 Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path/CS102)

### Day 25: May 23, 2021

**Today's Progress**
* Finished the CS101 Final Project for the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science).

**Thoughts**
* It is complete! Creating the win check for the diagonals was definitely the most complicated part of this game, and although it took me a minute to figure out how to do it efficiently, it is working flawlessly now. I also added in error handling for the inputs because if an integer was not entered, it would simply exit the program. Now it is set to reprompt, and if an integer is not entered again, that player forfeits the game, and the other player wins! This was definitely a fun little project.
* Being mainly a solo gamer, I was wondering if I could create an AI opponent for the game. In order to have the AI actually be intelligent, instead of just randomly placing pieces, it would take a fair amount of work that is beyond the scope of the actual project. This is something I will likely come back to implement, though, as it would be a nice challenge for sure.

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 24: May 22, 2021

**Today's Progress**
* Continued working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* Another successful day working on the project. I was able to complete the second win check, which is if there are four in a row in a column. I then started working on the win check for diagonals, which is a bit more complicated. While doing so, though, I realized I had no check in place for if the grid was completely full, meaning no more pieces could be placed resulting in a tie. I put this check in place, albeit not after spending way too much trying to figure out what was going wrong with it. Lo and behold, I made the silly mistake of looping through the list and not the range length of the list. After I figured that out, everything was working perfectly. Now all that is left is to finish the diagonal win check!

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 23: May 21, 2021

**Today's Progress**
* Continued working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* Today was a good day full of problem solving to figure out the best solution for a problem. While working on the check_win function, I went through a few different versions of the first piece, and the latest one now works perfectly. This includes a new function that is used inside of it, as well, and that piece will be used in the rest of the check_win function that has yet to be written. Now that I have the main system down for how I want this function to operate, I should hopefully be able to complete the final two parts of the check tomorrow.

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 22: May 20, 2021

**Today's Progress**
* Continued working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* To start the day off, I actually got to go through the process of reviewing and merging a pull request, which I have not had a chance to do before now, so that was a good process to learn. My biggest success of today was finally getting that choice validation to work correctly. After really thinking about it and talking about it out loud to a friend, I ended up figuring out exactly what I needed to before they even had a chance to reply. It was such a great epiphany! In the process of doing that, I was able to clean up a lot of the code, so now it is a lot easier to follow. All that is left to do now is create the check_win function and figure out one final nit-picky thing that is bugging me (if you enter a value that is not a digit, the program throws an error and exits).

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Status Update

This past week was a bit of a roller coaster. I had some medical issues arise, and my body did not respond well to the treatment at all. Both my physical and mental states were so out of balance, that I was unable to do hardly anything at all. Thankfully, my body is now starting to stabilize, which means I am able to actually think again and get back to programming! I can't wait to wrap up the CS101 Final Project.

Happy Coding, Everyone!

### Day 21: May 13, 2021

**Today's Progress**
* Continued working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* If there was ever a chasing your tail in programming, I think today was that day. What started out as being on the right path and making good progress ended in complete confusion as to why the program is behaving the way it is. I started by completing the choice validation to ensure there was no way that you could enter an incorrect value, and if you did, it would prompt as to what it was and ask you to enter a new value. This all worked flawlessly when testing it with hard set grid values, so it was time to implement the code that would find the next open row for the column selected, then place the piece according to the current player's number. This would work great unless a 0 was selected (valid options are 1-7) or a column was full. If 0 was selected, it would prompt accordingly, but no matter what column you chose next, it would always place your piece in the last column. This to me means that the column value is being set to -1, but I cannot tell where or why it is happening as of yet. If the column was full and you chose a column that was not full, it would give a TypeError saying it must be an integer or slice, not a NoneType, and exit the program. This really has confused me, as I am unsure where the value is being converted from an integer to None. Looks like tomorrow is going to be full of bug hunting!

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 20.5: May 12, 2021

**Today's Progress**
* Continued working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* Today I definitely went down a rabbit hole of tangents while working on the project, and I had a blast doing so. Although I did not get a ton of coding done on the project today, thus why I considered this to be a half day, I did learn some cool new tricks that I should be able to apply to the project when I resume working on it again tomorrow.

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 20: May 11, 2021

**Today's Progress**
* Started working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) CS101 Final Project.

**Thoughts**
* For the Python Terminal Game final project, I decided to create a terminal version of Connect Four. The main reason behind this is because I wanted to choose something that would not take weeks to program, so I could move on to the new content sooner, but would still provide a little challenge. Turns out this little game is not quite as easy as I was thinking it was going to be, which is actually quite nice. It is not terribly difficult by any means, but I am finding that the more I code it, the more checks and error handling I will need to put in place in order for it to operate smoothly. Overall, though, it has been a lot of fun trial and error thus far. I am hoping to finish it by tomorrow, now that I have the main framework in place.

**Link to work**
* [Python Terminal Game Repo](https://github.com/StingzLD/Python_Terminal_Game)

### Day 19: May 10, 2021

**Today's Progress**
* Started working on the [Computer Science Career Path](https://www.codecademy.com/learn/paths/computer-science) on Codecademy.

**Thoughts**
* Seeing as I have already completed the Learn the Command Line, Learn Git, and Learn Python3 courses, the vast majority of the CS101 part of the career path has already been completed. This left me with only a few additional items to go through, with one of them being a project utilizing all three of those courses. The only portion left of CS101 is the final project, an off-platform portfolio project called Python Terminal Game, which I will begin working on tomorrow.

**Link to work**
* [Computer Science Repo](https://github.com/StingzLD/Codecademy/tree/master/Computer_Science_Career_Path)

### Status Update

As you have noticed, it has been some time since my last commit, however it was not from a simple abandonment of the challenge from being too busy, not wanting to continue, etc. Instead, the past few weeks have been pretty rough with the sudden passing of my father-in-law, and as a result, this challenge took a backseat for obvious reasons. That being said, I feel like it is time to get my head back in the game and continue on with this challenge.

Reviewing where I left off, I believe I need to take a step back and look at different paths. Although the cybersecurity stuff was what I really wanted to get into, there is a lot of cybersecurity related items that are not coding related, and I do not want to start down that path in the middle of this challenge. Perhaps I will start a separate 100 Days challenge for myself later that is strictly cybersecurity related. With that in mind, there is still a lot that I have to learn about everyday Python programming, which will also make working on those cybersecurity tasks easier. There are also more relevant tasks I want to learn that would be more beneficial in the more immediate future (prospective jobs), so I want to start pursuing those instead. What exactly this will be is something I am going to work on figuring out today, then start working on that path tomorrow.

Happy Coding, Everyone!

### Day 18: April 13, 2021

**Today's Progress**
* Continued working on the [Port Scanner](https://www.freecodecamp.org/learn/information-security/information-security-projects/port-scanner) project on freeCodeCamp.

**Thoughts**
* Today was particularly challenging. I noticed that none of the calls in main.py actually had errors, so it was not testing the error handling. I decided to make both a domain and IP invalid to test, and for some reason, my error handling was only taking one path instead of actually changing depending on whether it is a domain or IP. I ended up finding that this is because it kept returning a socket.gaierror for both cases, and there seemed to be no good way to differentiate between the domain and IP. I tried a whole slew of different ways to check to see if the domain or IP was valid, using pretty much every solution I could find online, but they still kept returning the same socket.gaierror. After messing with this for about five hours, I finally found solution to what I thought was going to be a simple solution of differentiating between a domain and IP. Let me just say that this simple problem has a very simple solution, and I would probably feel ashamed if I was actually seasoned in non-embedded Python, but it literally came down to a single line of code that split the target (variable holding either the domain or IP) with a period, then evaluated if the last item in the list was a digit or not with the isdigit method. Not knowing about this, I clearly had no idea that was an option, but holy moly is this is lifesaver in this application! I immediately put it to use, tested it, and my error handling now worked flawlessly.

**Link to work**
* [Port Scanner](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/Projects/Port_Scanner)

### Day 17: April 12, 2021

**Today's Progress**
* Continued working on the [Port Scanner](https://www.freecodecamp.org/learn/information-security/information-security-projects/port-scanner) project on freeCodeCamp.

**Thoughts**
* I was able to get the majority of the port scanner completed tonight, which required me researching how to do certain things in Python like validating a URL or IP. Although this scanner should have been completed tonight, my brain kept running in circles when it came to what should be a simple task of creating the formatted verbose text. Since I was just spinning my wheels, I decided it would be best to get some shuteye, give my brain a break, and pick it back up in the morning with a fresh perspective.

**Link to work**
* [Port Scanner](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/Projects/Port_Scanner)

### Day 16: April 11, 2021

**Today's Progress**
* Completed the remaining lessons of [Python for Penetration Testing](https://www.freecodecamp.org/learn/information-security#python-for-penetration-testing) on freeCodeCamp.
* Started working on the [Port Scanner](https://www.freecodecamp.org/learn/information-security/information-security-projects/port-scanner) project on freeCodeCamp.

**Thoughts**
* After going through all of the pentesting lessons, two things are pretty clear. One, it takes very little code to perform tasks that I thought would be incredibly more involved. Two, there is a ton I still need to learn about the sockets module, and I will need to study that in depth at some point after this challenge is complete. Otherwise, I will be stuck studying for a few days, maybe weeks, instead of actually coding.

**Link to work**
* [My PenTesting Repo](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/PenTesting)
* [Port Scanner](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/Projects/Port_Scanner)

### Day 15: April 10, 2021

**Today's Progress**
* Finished the last of the [Inheritance and Composition: A Python OOP Guide](https://realpython.com/courses/inheritance-composition-python/) course on Real Python.

**Thoughts**
* I learned a lot from this course, as it covered a lot of material that was never even touched on Codecademy while initially learning Python. This course will definitely be one that I revisit once I start building programs from scratch to refresh on the lessons learned, as there is a lot of good info here.

**Link to work**
* [Inheritance and Composition Repo](https://github.com/StingzLD/Real_Python/tree/main/Inheritance_and_Composition)

### Day 14: April 9, 2021

**Today's Progress**
* Finished the majority of the [Inheritance and Composition: A Python OOP Guide](https://realpython.com/courses/inheritance-composition-python/) course on Real Python.

**Thoughts**
* Today was better symptom-wise, however I thought it would be best to continue with the video course, as there was a lot of good information there yesterday. Although I did not finish all of the videos today (there are nearly three hours worth for this course), I may finish them a little later tonight, so that I can focus solely on getting some coding done on the pentesting course from freeCodeCamp.

**Link to work**
* [Inheritance and Composition Repo](https://github.com/StingzLD/Real_Python/tree/main/Inheritance_and_Composition)

### Day 13.5: April 8, 2021

**Today's Progress**
* Completed the [Intro to Object-Oriented Programming (OOP) in Python](https://realpython.com/courses/intro-object-oriented-programming-oop-python/) course on Real Python.
* Completed the [Supercharge Your Classes With Python super()](https://realpython.com/courses/python-super/) course on Real Python.
* Started the [Inheritance and Composition: A Python OOP Guide](https://realpython.com/courses/inheritance-composition-python/) course on Real Python.

**Thoughts**
* Today was day two after getting my first COVID vaccine shot, and I ended up with a pretty bad headache that put me down for the count. Even though I know I would not be able to focus on writing code, I still made sure to at least do something related. I ended up back on Real Python to go over a few more tutorials to reinforce what I had previously learned at Codecademy.

**Link to work**
* None

### Day 13: April 7, 2021

**Today's Progress**
* Completed the Nmap Scanner lessons of [Python for Penetration Testing](https://www.freecodecamp.org/learn/information-security#python-for-penetration-testing) on freeCodeCamp.

**Thoughts**
* Seeing as there is a ton I still need to learn about sockets, I decided it was best to go back to the my freeCodeCamp projects. Today was developing a Nmap scanner, which of course had its fair share of hiccups. Although the video lesson made it seem like you just needed a single command (pip3 install python-nmap) to install the proper package, it ended up being a bit more than that. I kept getting error saying that nmap was not installed, and I could easily verify this because VS Code was not populating any of its modules. After a bit of research, I learned that Nmap itself also had to be installed (pip3 install nmap), as python-nmap referenced the module. Unfortunately, that was still throwing errors, and it took a random forum post to figure out why. Apparently, you have to install python-nmap as the user (pip3 install --user python-nmap). This finally allowed me to use the nmap module, but when running the script, it couldn't find what it needed in PATH. After reviewing the contents of PATH, the directory was indeed not there. I added directory location, but it was still giving the same error. It was only after I downloaded and installed Nmap directly from the website that it fully installed and populated PATH, then I had to reinstall python-nmap and restart the VS Code. Running the script was finally a success!
* Like the last time I went through a lesson, there was a lot of information left to be discovered on your own, as we never really got to understand the underlying modules we were using. Because of this, I have more research to do, so I can actually understand exactly what is going on when looking at the script, rather than having to rely on the person in the video to tell me what the code is doing. Only then will I truly be proficient at it.

**Link to work**
* [My PenTesting Repo](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/PenTesting)

### Day 12: April 6, 2021

**Today's Progress**
* Continued learning more about sockets in Python.

**Thoughts**
* Today I was learning about how to handle multiple connections, and although I did learn more, it only brought about even more questions because now I want to know everything there is to know about this new module used. This is why I have insomnia. I get so carried away with looking up this, which tangents to that and that and that and that, which splits off to all of those, and so forth. Time to real it back in to focus on sockets.

**Link to work**
* [My Socket Programming Repo](https://github.com/StingzLD/Socket_Programming)

### Day 11: April 5, 2021

**Today's Progress**
* Started learning more about sockets before continuing on with the pentesting course.

**Thoughts**
* After a very rough few days for personal reasons, I was very happy to get back to coding, only to run into issues when trying to run the Python scripts in the VS Code terminal. Depending on the type of terminal, it would either just open the code in a VS Code tab (or go into the tab if it was already open) or give me a 'Permission Denied' error. After spending way too much time looking for a solution, I just decided to reinstall Git, as that seemed to be the biggest issue (the one providing the permission error). After reinstalling Git and relaunching VS Code, I was able to run the scripts without issue. I am thinking the Windows Updates caused an issue with it, but I will never know for sure. Either way, I was finally able to test my two new scripts side-by-side in VS Code successfully.

**Link to work**
* [My Socket Programming Repo](https://github.com/StingzLD/Socket_Programming)

### Day 10: April 1, 2021

**Today's Progress**
* Completed the first three parts of [Python for Penetration Testing](https://www.freecodecamp.org/learn/information-security#python-for-penetration-testing) on freeCodeCamp.

**Thoughts**
* I really wish this would have been a little more in depth with the intro, as the videos dive you right on in, as if you already know what the functions and methods do. The video roughly explains the pieces we are using, but only at a very high level. There will definitely be more studying required to fully understand the socket library.

**Link to work**
* [My PenTesting Repo](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/PenTesting)

### Day 9: March 31, 2021

**Today's Progress**
* Completed [Information Security with HelmetJS](https://www.freecodecamp.org/learn/information-security/information-security-with-helmetjs/) on freeCodeCamp.

**Thoughts**
* Admittedly, this took me a bit to initially figure out, as I had to look up JS syntax on top of HelmetJS and BCrypt because I have not learned any of those yet. Nonetheless, I was able to successfully complete the challenges, which ended up being fairly easy once working with basic JS was no longer an issue. That being said, I am sure I will probably have to go back and look at the HelmetJS and BCrypt documentation in the future to refresh on how to configure and use the packages, but it is fairly straightforward once you have the information in front of you.

**Link to work**
* [My HelmetJS Repo](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/boilerplate-infosec)
* [My HelmetJS Repl.it](https://replit.com/@StingzLD/boilerplate-bcrypt)
* [My BCrypt Repo](https://github.com/StingzLD/freeCodeCamp/tree/master/Information_Security/boilerplate-bcrypt)
* [My BCrypt Repl.it](https://replit.com/@StingzLD/boilerplate-infosec)

### Day 8: March 30, 2021

**Today's Progress**
* Completed the remaining [Learn Python 3](https://www.codecademy.com/learn/learn-python-3) Code Challenges: Dictionaries, Dictionaries (Advanced), Classes, Classes (Advanced).

**Thoughts**
* The remaining challenges were pretty low in difficulty, like the others, with the exception of Classes (Advanced). The only reason I say this, however, is because Codecademy had flaws in their instructions, so I had to figure out what exactly the tests were looking for then figure out how to change the code to reflect that. In that regard, it made it slightly more challenging, but it was also good practice in debugging using a test result.
* I also had my first big issue with Git today. I work on multiple machines, and I have the repos cloned on all of them. Tonight, I made a commit without first pulling, which then showed the commit message as merging. Considering this is not what I wanted, I wanted to undo the commit. I found that to do this you have to do a "git reset --hard HEAD~1", which I did, but it did not undo the merge it created when I pulled everything down. I decided to run it again to get rid of that, as that was the only commit still showing up for today, and although it got rid of that merge, it actually got rid of the previous commit as well! Luckily, I backed up my files before doing anything, so I just put those back in and made a new commit, but now my commit history is missing a commit, which makes it look like I did nothing that day. Ugh... Lesson learned. BE CAUTIOUS WHEN DOING A HARD RESET!!!

**Link to work**
* [Code from Codecademy challenges](https://github.com/StingzLD/Codecademy/tree/master/Python3/Code_Challenges)

### Day 7: March 28, 2021

**Today's Progress**
* Completed the following [Learn Python 3](https://www.codecademy.com/learn/learn-python-3) Code Challenges: Strings, Strings (Advanced).

**Thoughts**
* These challenges were a good refresher on functions I have not fully utilized since originally learning them.

**Link to work**
* [Code from Codecademy challenges](https://github.com/StingzLD/Codecademy/tree/master/Python3/Code_Challenges)

### Day 6.5: March 27, 2021

**Today's Progress**
* Watched a few videos from freeCodeCamp on YouTube.

**Thoughts**
* Due to some personal reasons, I was not in a mindset that would allow me to really focus on coding today. However, I did at least spend some time watching related videos.

**Link to work**
* None

### Day 6: March 26, 2021

**Today's Progress**
* Completed the following [Learn Python 3](https://www.codecademy.com/learn/learn-python-3) Code Challenges: Loops, Loops (Advanced), Functions, and Functions (Advanced).

**Thoughts**
* Although most of the challenges were of the same difficulty (or lack thereof) as yesterday, there was one in the Loops (Advanced) that actually caused me to think about how I would go about doing it, as I had to recall the ways a certain function behaved that I have not used for a little while. Overall, though, it was good practice to refresh my brain on lessons learned earlier in the course that were not used much in later lessons.

**Link to work**
* [Code from Codecademy challenges](https://github.com/StingzLD/Codecademy/tree/master/Python3/Code_Challenges)

### Day 5: March 25, 2021

**Today's Progress**
* Completed the following [Learn Python 3](https://www.codecademy.com/learn/learn-python-3) Code Challenges: Control Flow, Control Flow (Advanced), Lists, Lists (Advanced).

**Thoughts**
* After completing the course yesterday, I noticed that there were two new sections in the course: Python Code Challenges and Python Code Challenges II. Naturally, I decided to take these on! After all, who am I to turn down a challenge. I mean, that is exactly how I ended up doing the 100DaysOfCode challenge in the first place! Sadly, though, the challenges were not very challenging so far, even the "advanced" ones.  Granted, there is only so complicated control flow and manipulating lists can get within the context of the course, but they still seemed a bit too easy. Up next are challenges for loops and functions, so hopefully those be more of a brain teaser.

**Link to work**
* [Code from Codecademy challenges](https://github.com/StingzLD/Codecademy/tree/master/Python3/Code_Challenges)

### Day 4: March 24, 2021

**Today's Progress**
* Finished the [Learn Python 3: Function Arguments](https://www.codecademy.com/courses/learn-python-3/lessons/learn-python-function-arguments) Codecademy lesson.
* Completed the [Learn Python 3: Function Arguments](https://www.codecademy.com/courses/learn-python-3/lessons/learn-python-function-arguments) Codecademy project.
* Completed the [Learn Python 3](https://www.codecademy.com/learn/learn-python-3) Codecademy class!!!

**Thoughts**
* The rest of the Function Arguments' lessons taught some very good ways to process code, as well as minimize the amount of code needing to be written.
* I am SO HAPPY that I have now completed the Learn Python 3 course from Codecademy!!! The question is, where do I want to go from here? I need to get work done on my CMMC Assessment Tool conversion side project, but there are also a couple of courses on freeCodeCamp that I want to pursue, specifically [Information Security](https://www.freecodecamp.org/learn/information-security/) and [Data Analysis with Python](https://www.freecodecamp.org/learn/data-analysis-with-python/). My current job is IT security, and I have been really wanting to get into using Python for scripting changes to the infrastructure, so that seems like the logical next step. What better way to build Python knowledge than while building tools to help with my job. On the flipside, I really want to start exploring data analysis with NumPy, Pandas, etc. Ultimately, I think both courses are going to be highly beneficial, as parsing through data collected in CSVs from multiple programs and making sense of it all is also a big part of my job.

**Link to work**
* [Code from Codecademy lesson](https://github.com/StingzLD/Codecademy/tree/master/Python3/11.Function_Arguments/Lesson)
* [Code from Codecademy project](https://github.com/StingzLD/Codecademy/tree/master/Python3/11.Function_Arguments/Project)
* [Certificate: Learn Python 3 Course](https://www.codecademy.com/profiles/stingzld/certificates/6c152bd262967f8c941c9707ed636bda)

### Day 3: March 23, 2021

**Today's Progress**
* Worked through most of the [Learn Python 3: Function Arguments](https://www.codecademy.com/courses/learn-python-3/lessons/learn-python-function-arguments) Codecademy lesson.

**Thoughts**
* A lot of this lesson seemed to be just repeat material from earlier in the course with a twist, until the later lessons. There was not a lot of writing code, though, mainly just reading the explanations in the lessons (a lot of text to read in these lessons), going through the code, and find things to change. Not necessarily a bad thing, per se, but I was expecting the final lesson of the course to be much more jam packed with coding.

**Link to work**
* [Code from Codecademy lesson](https://github.com/StingzLD/Codecademy/tree/master/Python3/11.Function_Arguments/Lesson)

### Day 2: March 22, 2021

**Today's Progress**
* Completed the [Learn Python 3: Classes](https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-classes) Codecademy project.

**Thoughts**
* I seem to be in a limbo state where I understand the concept, I can create class structures and objects based off of them without issue, but I still have that feeling that I am missing something. Based off of this project, I really have no reason to feel that way. Perhaps it is because I am still being fed the information like the class names, parameters, etc., so I have not actually had to create everything from scratch-scratch yet, even though I was able to write all of the code in this project without assistance.

**Link to work**
* [Code from Codecademy project](https://github.com/StingzLD/Codecademy/blob/master/Python3/10.Classes/Project/BastaFazoolin.py)

### Day 1.5: March 21, 2021

**Today's Progress**
* See "Thoughts"

**Thoughts**
* Decided to spend time researching more about OOP to deepen my understanding before continuing on.

**Link to work**
* No coding performed today.

### Day 1: March 20, 2021

**Today's Progress**
* Walked through Object Oriented Programming tutorials on [Real Python](https://realpython.com/python3-object-oriented-programming/) and [W3Schools](https://www.w3schools.com/python/python_classes.asp), and went through their exercises. 
* Reset and went through the [Learn Python 3: Inheritance and Polymorphism](https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-classes) Codecademy lesson again.

**Thoughts**
* The reason for finding additional tutorials and resetting the Codecademy lesson is because it simply was not clicking last night. I was able to complete the lesson by following the examples in the instructions, but there were parts that my tired brain was just not comprehending. Now that I am going through everything with a fresh brain, everything is clicking.

**Link to work**
* [Code from Codecademy lesson](https://github.com/StingzLD/Codecademy/tree/master/Python3/10.Classes/Inheritance_and_Polymorphism)

### Day 0: March 19, 2021

**Today's Progress**
* Forked the 100 Days of Code repo, and edited it accordingly.
* Created a new repo for my CMMC Assessment Tool conversion.
* Learned how to format Markdown, and created a proper README.md for the repo.
* Finished the Codecademy course "Learn Python: Inheritance and Polymorphism".

**Thoughts**
* Although I understand Markdown is supposed to be simplistic, the inability to use multiple spaces while formatting text is rather frustrating.

**Link to work**
* [CMMC Assessment Tool's README.md](https://github.com/StingzLD/CMMC_Assessment_Tool/blob/master/README.md)
* [Learn Python 3: Inheritance and Polymorphism](https://www.codecademy.com/learn/learn-python-3/modules/learn-python3-classes)
