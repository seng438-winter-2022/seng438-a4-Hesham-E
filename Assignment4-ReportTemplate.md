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

# A discussion on the effect of equivalent mutants on mutation score accuracy



# A discussion of what could have been done to improve the mutation score of the test suites

# Why do we need mutation testing? Advantages and disadvantages of mutation testing

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

# How the team work/effort was divided and managed


# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
