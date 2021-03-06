<a name=toc></a>
## Table of Contents
* [Professional Self-Assessment](#psa)
* [Informal Code Review](#icr)
* [Artifacts](#artifacts)
  * [Software Engineering, Design, Data Structures, and Algorithms](#seddsa)
  * [Database](#db)

<a name=psa></a>
## Professional Self-Assessment
This portfolio helps to provide insights into some of the work that I have done while a student at Southern New Hampshire University (SNHU), helps to showcase my growth over the past three years as a software developer, and helped to solidify my goals while completing this project and the overall coursework.

Prior to entering the Computer Science program at SNHU, I had no practical or theoretical experience within the world of software engineering; however, over the past 3 years I have been able to complete all of the classes for the computer science program, attend of coding boot camp, get accepted into a software development engineering apprenticeship role at Amazon, and finally get hired on full-time as a software development engineer at Amazon on the Alexa Health Consumer team.

The coursework has provided me with many areas of new knowledge; however, three of the most important concepts and skills I have gained over the course of the past 3 years have been 1) agile development methodologies; 2) software testing, automation, and quality assurance; and 3) collaboration and team project work. For me, agile development methodologies have been an incredibly important topic to learn and master. The team I am on at Amazon utilizes the agile development methodologies to help organize our team’s structure and development practices. Without the prior knowledge I learned at SNHU, I do not believe I would be as successful in my current position as I am now. Software testing, automation, and quality assurance have also been incredibly important in my growth and success as a developer. The lessons I learned and tools I gained while at SNHU have helped me to be successful in my coding boot camp and in my job – understanding the importance of testing best practices and how to apply that to my development has been a major improvement to my coding standards and help me to succeed in person development and knowing how to actively assist members of my team. Finally, the lessons in collaboration and team project work provided me the foundations I needed to write and provide effective code reviews. The use of code reviews is an essential piece of the development process and is one that I use often at work. I do not believe my understanding of code reviews – specifically how to create a well formatted response and single topic review would have been as strong as it is now if I had not participated in this program at SNHU.

Outside of the coursework, I have also had the opportunity to attend a coding boot camp – Code Fellows – as a part of my apprenticeship program for Amazon. This opportunity provided me with the practical coding skills and in-person collaboration skills that I learned about while at SNHU. This was an incredible way to meld together the theoretical with the practical and build out a comprehensive portfolio. This also provided me with a unique opportunity to work at one of the major tech companies, while still learning. The main areas of learning at the coding boot camp where in coding practice for JavaScript, PostgreSQL, React, React, Java, Sprint, Amazon Web Services (AWS) development, data structures and algorithms, and secure coding techniques. The hands-on learning culminated in four major collaborative coding projects – [Clever Gyro](https://github.com/falafel-raptors/clever-gyro), which is a JavaScript web application where you attempt to reach a target number by combining randomly generated numbers using addition, subtraction, multiplication, division, and modulos; [Fantasy Wordbook](https://github.com/cinnamonizers/fantasy-wordbook), which is a React and PostgreSQL web application which pulls from various APIs to allow a user to get the definitions, usage, and examples of any word found in the Lord of the Rings or Bhagavad Gita; [helloHome](https://github.com/kenipesa/helloHome), which is a Java and Spring web application which provides basic financial information to users looking to purchase a new home; and [Feed Me Now](https://github.com/TeamCodebreakers/IDK), which is an Alexa Skill which provides restaurant choices to people who have a hard time deciding where to eat.

As a culmination of all of this prior work – both at SNHU and in my coding boot camp – I had to choose projects which needed improvements to provide the code reviews for the artifacts section of this portfolio. I decided to focus on two projects I completed while at SNHU – the Zoo Monitoring System developed in the IT 145: Foundations in Application Development course and the Mobile2App Weight Tracker Android app which I developed in the CS 360: Mobile Architect and Programming course. I chose these two applications because they offered me the best opportunity to showcase areas of growth and improvement. The Zoo Monitoring System was the focus for both the Software Engineering and Design section and the Data Structures and Algorithms section. This encompassed both because I developed this application before learning best practices in both areas and was a way for me to showcase my learnings in those areas. The Mobile2App Weight Tracker app was the focus for the Database section because it was one of the only projects developed using a database and it suffered from a variety of database issues which needed to be addressed to improve the applications security and efficiency.

[[Return to Top]](#toc)

<a name=icr></a>
## Informal Code Review
[![informal code review video link](./informal_code_review_image.png)](https://youtu.be/QKprOsAyLFM)
[[Return to Top]](#toc)

<a name=artifacts></a>
## Artifacts
<a name=seddsa></a>
### Software Engineering, Design, Data Structures, and Algorithms
For this artifact I have chosen the [Zoo Monitoring Command Line Interface (CLI)](https://github.com/paronicholas/ZooMonitorSystem), a Java based application, which I first developed in the IT 145: Foundations in Application Development course. This application allows a user to monitor different aspects of the zoo – either the animals or the habitats – and provides information about the different aspects being viewed. Within those aspects the user can see if there are any areas of alert for the animals or habitats – either missing fields or areas of concern. This application reads information about the animals or habitats from text files containing a title section, which helps to populate the individual monitoring menus and information about each animal or habitat.

I chose this application because it provided the best opportunity for improvement within a completed application and offered a change for me to showcase areas of growth with regards to my utilization and understanding of software engineering and design principles. When I first wrote this application, I did not have any prior knowledge of Java or object-oriented development. As such, this application was not cleanly developed and has a lot of areas which can be improved upon. One of the most significant areas for improvement is the overall design of the application – file organization and structuring of classes. Over the course of the past year-and-a-half I have attended a coding boot camp and begun employment as a software development engineer at Amazon and have made many strides in my development practices, especially in the areas of incorporating strong object-oriented development designs and ensuring I follow Java best practice standards. 

I also chose this application because it offered me the ability to improve upon the Data Structures and Algorithms portion as well. A major piece of the re-design was to improve upon the class structure and identify areas of improvement for efficiency – an increase in efficiency often comes from choosing the correct data structures and using appropriate algorithmic development. This helps to reduce the time and space complexity of the application. For this application, I needed to develop a much more efficient and error resistant structure when importing the data from the text files for the animals and habitats. I decided to tackle both the design and data structure components at the same time for this because the improvements relied upon the other and allowed me to make the application much more seamless and easier to follow.

One of the major improvements of the application was in the design of the application. Below is the improvement to the overall class structure:
#### Initial Application Structure
```
src/main/java
 |- Main.java
 |- Menus.java
 |- Monitors.java
 |- Parsers.java
 |- animals.txt
 |- habitats.txt
```
#### Re-designed Application Structure
```
src
 |- main/java
  |- helper
   |- MonitorSystemOutputStatic.java
   |- Parse.java
  |- menu
   |- MainMenu.java
   |- Menu.java
   |- MonitorMenu.java
  |- monitor
   |- Animal.java
   |- Habitat.java
  |- system
   |- MainSystem.java
   |- MonitorSystem.java
  |- text
   |- animals.txt
   |- habitats.txt
  |- Main.java
 |- test/java
  |- helper
   |- ParseTest.java
```
For the main focus of the data structures and algorithms refactor I mainly focused on the `Parse.java` class. In the initial implementation of this class, the Parse class read was called every time a monitor was chosen. The parsing method - `monitorInfoParser` would loop through a list of strings, retrieved from the specified text file, and then remove everything prior to the expected animal or habitat.
```java
void monitorInfoParser(List<String> parsableList, int choiceNumber, int mainMenuOption) {
        List<String> monitorInfoList = new ArrayList<>(Collections.emptyList());
        int[] monitorInfoLength = new int[2];

        monitorInfoLength[0] = 4;  // Length of animal monitor for iteration
        monitorInfoLength[1] = 3;  // Length of habitat monitor for iteration

        // Assigns call variables to user chosen monitor option
        for (i = 0; i < choiceNumber; ++i) {
            for (j = 0; j <= monitorInfoLength[mainMenuOption - 1]; ++j) {
                monitorInfoList.add(parsableList.get(0));
                parsableList.remove(0);
            }
        }

        // Removes parsed monitor information prior to user chosen monitor option
        for (i = 0; i < choiceNumber - 1; ++i) {
            for (j = 0; j <= monitorInfoLength[mainMenuOption - 1]; ++j) {
                monitorInfoList.remove(0);
            }
        }

        System.out.println("------------------------------");

        // Creates alert for out-of-normal information and removes "*" from index string
        for (i = 0; i <= monitorInfoLength[mainMenuOption - 1]; ++i) {
            if (monitorInfoList.get(i).contains(ALERT_CHARACTERS)) {
                alert = monitorInfoList.get(i).replace(ALERT_CHARACTERS, "");
                monitorInfoList.set(i, alert);  // Replaces index string with "*" with same index string without "*"
                System.out.printf("ALERT - %s - ALERT\n\n", alert.toUpperCase());
            }
        }

        for (i = 0; i <= monitorInfoLength[mainMenuOption - 1]; ++i) {
            System.out.println(monitorInfoList.get(i));
        }
        System.out.println("------------------------------\n");
    }
```
This implementation did not offer any error handling or provide any reliability in the system if a user input the incorrect information into the text file. For the refactor, I extracted out the different portions of this method into helper functions and used the new `Animal` and `Habitat` objects created in the software engineering and design refactor to dynamically build a list of `Animal` or `Habitat` objects to be used for the chosen monitor menu. This refactor allowed me to add in additional error handling, ensure that all `Animal` or `Habitat` objects had the same structures, and improved the overall efficiency by reducing the number of times the text files needed to be parsed while the system was running. The new structure, and stack tracing, can be followed from the [buildAnimalList](https://github.com/paronicholas/ZooMonitorSystem/blob/master/src/main/java/helper/Parse.java#L71) method or the [buildHabitatList](https://github.com/paronicholas/ZooMonitorSystem/blob/master/src/main/java/helper/Parse.java#L97) method.

I believe that the improvements I have made to the Zoo Monitoring System have met the course objectives for improving upon the Software Engineering and Design and Data Structures and Algorithms of the application. The updates to the Zoo Monitoring System improve the overall design of the application so that it follows 0bject-0riented development designs, uses class structuring, follows secure coding practices – to include the use of the correct member access types, and utilizes test cases to ensure code reliability. Additionally, the improvements have improved upon the data structure and reliability of the Parser class so that it is not generating the animal or habitat readouts after the user selection has been made – the system now employs the use of programmatically generated Animal and Habitat objects which are built when the user chooses a monitor option. This creates stability within the code and adds additional error. Additionally, the methods throughout the code base have been reworked so they follow the single use principle. This allows the code to be more readable and reduces the chance for errors.

As I was going through this process, I realized that the initial feature was a good starting point, but needed more work than originally envisioned. I was also able to see how much I have improved as a developer since originally writing this application. I was able to take my design document and easily translate it into meaningful class structure and connect the classes in a way that made sense. I also re-learned that refactoring a code base with little direction takes a lot of patience and not every idea I had envisioned worked during the refactor. I had originally intended on the Animal and Habitat classes to extend a parent class; however, after attempting to create a parent class I found that it would have been more effort than necessary and the reduction in complexity would have been minute in comparison to the effort involved. I abandoned this idea after a quick cost-benefit analysis and feel that the compromise of a few conditionals and Lists was worth the reduction in time spent. If this system were to be adapted to a much larger monitoring system, I would spend the time to create a more robust parent class system that would allow for the different types of monitors to fall under the single parent; however, the size of this system did not justify that expense. Finally, I realized there is always additional areas for improvement, even after the refactor has been completed. This became very apparent in the Parser class after I created the `buildAnimalList` and `buildHabitatList` methods. These methods are almost identical – except for their return types and the number of properties added to each object. I found that both these methods could benefit from additional refactoring so that the reused sections benefitted from the single use principle. This helped to simplify the methods and make them easier to understand and follow.

[[Return to Top]](#toc)

<a name=db></a>
### Database
For this artifact I chose the [Mobile2App Weight Tracker Android app](https://github.com/paronicholas/WeightTracker), a Android/Java based application, which I first developed in the CS 360: Mobile Architect and Programming course. This application is a simple weight tracking phone app which allows a user to create an account or log in, add a target weight, add daily weight records, and view the logged weights in a logbook. I have chosen the Weight Tracker Android phone application because it is one of the only applications I developed while at SNHU that contains a database, and other applications I have created using databases all contain no-SQL databases, such as AWS DynamoDB and already follow best practices for structure and implementation. I felt that the use of the SQL database for the Weight Tracker was a good starting point and required the most improvement in order to get the system working. This component will be used to showcase my ability to create and access a database for a mobile application, which is not an area I have showcased in previous work on my GitHub page. This is my first non-web-based mobile application I have developed and showcases a different set of skills. The areas of focus for improvement in this application included:
* [zero-index error](https://github.com/paronicholas/WeightTracker/commit/8bf5a266354926aefa59097875824d28850971b5#diff-c28b91864d35b83e735513feafc343959dfeda79c0e4ae15fffd9d01899a1542L53) when creating a new user account row within the accounts table
* [getAccountByUsername](https://github.com/paronicholas/WeightTracker/blob/master/app/src/main/java/com/example/weighttracker/database/helper/WeightTrackerDatabase.java#L121) method for the accounts table
* [getDailyWeightsByAccountId](https://github.com/paronicholas/WeightTracker/blob/master/app/src/main/java/com/example/weighttracker/database/helper/WeightTrackerDatabase.java#L178) method for the daily weights table
* [getTargetWeightByAccountId](https://github.com/paronicholas/WeightTracker/blob/master/app/src/main/java/com/example/weighttracker/database/helper/WeightTrackerDatabase.java#L239) method for the target weight table

I believe the improvements I have made to the Weight Tracker have met the course objectives for improving upon the Database design of the application. The updates to the Weight Tracker have removed the zero-index issue from the database by implementing an auto incrementing primary key and a check to ensure the password and username for the attempted login match with an existing account. This verification prevents login if the username matches and the password does not, allows login if both matches, and creates a new user if neither match an existing user. This adds another layer of security to ensure that the attempted user must enter the correct information to access the account. The next improvements increase the efficiency of the application and improve data security. The database queries now match the account id collected from the login to match to the database. If records within the database exist and match the account id then they are returned and if they do not match the account id then they are not returned. This prevents a user from accessing another’s data and being able to modify or delete the information. 

This process of enhancement closely followed the improvement plan I developed in week 1’s plan. I updated the table creation strings to include an auto increment notation to ensure the data entries had the correct id column. This problem fixed the zero-index issue for the login feature. Once this was created, I performed an additional update to ensure that the login successfully matched username and password to gain entry to the requested account. After this, I began work on the additional methods to implement. I added a `getAccountByUsername` method for the account table to ensure I was only grabbing the correct account based on the user’s input username. The next improvements added a `getDailyWeightByAccountId` for the daily weights table and `getTargetWeightByAccountId` for the target weight table. These improve the applications efficiency and security by returning only the information associated with a specific account and not needing to create Lists of all the data within the database and then looping through that data to return the correct information. I ran into a few errors while correctly returning the data, specific database out of bounds errors; however, I was able to overcome these issues by performing a `Cursor moveToFirst()` check instead of a not null check. I was able to find a fix for the Cursor index out of bound exception by following the reference found in the Stackoverflow answer for the question [Android Cursor Index out of Bound Exception](https://stackoverflow.com/questions/17633091/android-cursor-index-out-of-bound-exception). The top answer provided the information to create a boolean check – if there was an entry to return the `Cursor moveToFirst()` would return true, else it would be false. This eliminated the out of bound exception.

[[Return to Top]](#toc)
