**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#4 – Mutation Testing and Web app testing**

| Group \#:  12    |     |
| -----------------| --- |
| Tom Altankhuyag  |     |
| Hasan Mahtab     |     |
| Asma Hashmi      | 30093995    |
| Hesham Elkaliouby|     |

# Introduction
This lab consists of two parts: Mutation Testing and GUI Testing. The first part will allow students to learn about mutation faults in a Java code-base with the mutation testing tool. It will also allow the student to interpret and report mutation scores, which will further allow students to design new test cases to improve the overall test suite quality. 
Part two will focus on the GUI testing automation. Student will use an extension called Selenium and will use that to test web interfaces and compare. 

# Analysis of 10 Mutants of the Range class 

# Report all the statistics and the mutation score for each test class



# Analysis drawn on the effectiveness of each of the test classes
For DataUtilites, the test cases seemed to already be quite effective since we started with a mutation coverage score of 83%. We created additional test cases to increase our mutation score to 85%, but it seems that the mutatnts that are left are either equivalent mutants or mutants that are protected by guard conditions that conventional test cases cannot reach. For example, some of the mutants removed a guard condition from the functions that disallows null parameters. We cannot test this with a conventional test case since null parameters are normally not allowed and PIT Test does not run with JUnit test cases that fail.

# A discussion on the effect of equivalent mutants on mutation score accuracy
The presence of equivalent mutants makes the performance of the test suite seem lower than it actually is. For example, an extremly common equivalent mutant was changing the looping condition on a for loop to be != rather than <. In a loop where the variable is incrementing with each run, the two guard conditions are the same because they become not true on the same run. However, having equivalent mutatnts might be illuminating to testers since they show what behavior is not allowed in future code changes. Going back to the example of the loop, if the < changed to a != on a decrementating loop, a null exception would occur since certain values would be out of range.

# A discussion of what could have been done to improve the mutation score of the test suites
To get increased mutant coverage, we analyzed the mutants side by side with the source code to see how it changed. Then, we created test cases to directly address the mutants, where possible. For example, a really common mutant was incrementaing numbers by one or decrementing them by one. In this context, we created test cases that would have the expecting value be outside that range of +-1. 

# Why do we need mutation testing? Advantages and disadvantages of mutation testing
Mutation testing provides advantages where it changes source code to illuminate edge cases that the testers that may have not thought about. For example, changing conditions to be somewhat similar could bring forth edge cases testers may not have thought of like changing a guard condition that is used for iterating the array to be one more would result in a boundary error. This boundary error should be accounted for in user programs in order to be able to recover from faults where a user may use an array that is abnormally large or abnormally small. We feel this is the reason that we need mutation testing because it shows cases that are really close to the source code, but could cause faults or errors during runtime that may not be recoverable.

A disadvantage of mutation testing is when it changes source code in a way that cannot be tested as outlined above. Equivalent and unreachable mutants cannot be conventially tested due to the nature of the tools as mentioned. This creates the impression that the test suite is not as effective as it should be, and when there are other people working on a team, it may seem that the testers are not doing their job properly.

# Explain your SELENUIM test case design process

The testing process for part 2 began on walmart.ca and bestbuy.ca, where the group decided to test 8 different functionalities. Every member chose 2 functionalities and tested them, and sent over the results. These results were confirmed on everyones devices. The 8 functionalities that were tested:

1. Bad email when registering for an account (Walmart)
2. Bad password when registering for an account (Walmart)
3. Testing the store finder (Walmart)
4. Searching for a specific item, ie.lawn chair (Walmart)
5. Using the search feature to check if searching "computer" will display computers and laptops (Bestbuy)
6. Using the category feature to guide through the website and find the graphics card section (Bestbuy)
7. …
8. …

After throughly going through each test case, the team decided to go through the weaker test cases and replace them for efficiency. Through this, the team was able to create 8 strong test cases, 2 for each member, which covered different areas of the site.


# Explain the use of assertions and checkpoints

Both checkpoints and assertions are automatically generated through the Selenium IDE. The endpoints display a checklist/step-by-step process of how the test case are generated. This ensures that each test case is done in a particular way, and the steps are broken down for simplicity sake. Both areas are important as they are responsible to reach the correct output, but also ensure that this output is reached correctly. This is crucial as there are times that an output is reached, but in the wrong order, which can lead to a failed test. The general idea is, if the steps were shown to someone else, they should be able to follow the steps easily and generate the same output. 

Below are the automated verification steps for each test case:

Test 1:

![Screen Shot 2022-03-18 at 5 54 56 PM](https://user-images.githubusercontent.com/82603082/159097975-68edfb01-8758-4331-a8a1-82eea457e754.png)

![Screen Shot 2022-03-18 at 5 55 23 PM](https://user-images.githubusercontent.com/82603082/159097989-24a02fe5-dfc1-4b14-b523-f49b59d75158.png)


Test 2:
![Screen Shot 2022-03-18 at 6 56 46 PM](https://user-images.githubusercontent.com/82603082/159100481-f0042367-d2fb-4081-85c4-80d0f6afa31f.png)

![Screen Shot 2022-03-18 at 6 56 52 PM](https://user-images.githubusercontent.com/82603082/159100482-cd5b0663-5368-40a0-a69e-a7c43a2a191f.png)

Test 3:

![Screen Shot 2022-03-18 at 5 38 18 PM](https://user-images.githubusercontent.com/82603082/159097170-709ebc8d-d774-42d8-9fea-550af16c7c8e.png)

Test 4:

![Screen Shot 2022-03-18 at 5 39 51 PM](https://user-images.githubusercontent.com/82603082/159097252-344acb22-a6a0-4e4f-b95d-f5974c4ad5e5.png)


Test 5:

![Screen Shot 2022-03-18 at 5 41 07 PM](https://user-images.githubusercontent.com/82603082/159097319-6f41c670-c448-4708-8dad-56ec8d02f68c.png)

Test 6:

![Screen Shot 2022-03-18 at 5 41 46 PM](https://user-images.githubusercontent.com/82603082/159097343-23515e4d-666c-403e-a433-829f8b52b7c5.png)


Test 7:

Test 8:

# how did you test each functionaity with different test data

# Discuss advantages and disadvantages of Selenium vs. Sikulix

There are a couple of advantages and disadvantages for both Selenium and Sikulix:
For Selenium, it uses a set of tools to automate testing of Web Applications. The user locators (id, classname, etc.) from HTML code are used to automate testing of Web Page Applications. Selenium uses regression testing, and it allows us to create an automation framework using testNG for reporting. Lastly, it supports all browsers and cannot automate desktop applications.
As for Sikulix, it uses tools to automate based on the GUI. It uses image recognition techniques internally and it requires images to be stored for image recognition. Lastly, it might react differently if an imaged saved matches more than one object on the screen.

As such, it is clear that Sikulix compared to Selenium is not the best as it requires image storage to be used for image recognition within a web page. Also, it is not the best with reading texts compared to Seleniums' HTML operation. Lastly, Sikulix is far less applicable compare to Selenium as it uses RPA instead of HTML/XML

# How the team work/effort was divided and managed



# Difficulties encountered, challenges overcome, and lessons learned

There were several difficulties encountered during the duration of this lab. Firstly, setting up the Eclipse environment for this lab was very tedious and it led to different errors for each group member. For instance, when trying to upload external jars, some jars were not provided for this lab, making it difficult to run the PIT mutation test as it would display “closed server” each time. This would lead to excessive time being wasted to resolve the problem. When this would happen, we as a group would spend hours trying to figure out why that may be the case. Thankfully, we were able to get it to work on two out of four laptops. As well, many of the group members faced difficulties when running all the methods at once. It worked for some, and didn’t for others. The PIT summary window would sometimes disappear when running the mutation tests, and figuring out how to get that back was difficult. As well, the running of PIT mutations was time consuming and lead to a lot of CPU usage. 

As for Part 2, there were times that Selenium would freeze up and not allow us to record our tests. To resolve this, we would have to quit Selenium and re-launch. Additionally, when playing all the tests recordings on Selenium, sometimes it would not play the recording, so we would have to recreate the entire project once again. 
In the end, our group invested a lot of time figuring out the errors and resolving. Some lessons learned were how to increase the mutation test coverage and GUI testing using a chrome extension.

# Comments/feedback on the lab itself

This lab was very time-consuming and required a lot of troubleshooting. As well, the instructions for setting up Eclipse for this assignment was very unclear, leading to additional problems. 
After getting past these problems, we got insight on how mutation testing works and how this is used to further improve test suites.
