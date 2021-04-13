# 100 Days Of Code - Log
*** Note: Any day that specifies "Day xx.5" refers to a day that was mainly full of research, and not so much coding. Since this challenge is to code for one hour a day, I would feel like I was cheating if I was to use those days as actually part of the challenge, even though there was still plenty of learning happening. Regardless, those days and related notes are still present in this log as a reminder of what all was learned and to show that progress was still being made, rather than their just being gaps in the log. ***

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
