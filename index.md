## Professional Self-Assessment

## Informal Code Review

## Artifacts
### Software Engineering and Design
For this artifact I have chosen the [Zoo Monitoring Command Line Interface (CLI)](https://github.com/paronicholas/ZooMonitorSystem), a Java based application, which I first developed in the IT 145: Foundations in Application Development course at Southern New Hampshire Univeristy. I chose this application because it provided the best opportunity for improvement within a completed application and offered a change for me to showcase areas of growth with regards to my utilization and understanding of software engineering and design principles. For this portion of improvements, I focused on re-designing the structure of the application to better follow object-oriented design principles and class based structures. The re-design also incorperated my learning of test-driven development and secure coding principles.

One of the major improvements of the application was in the design of the application. Below is the improvement to the overall class structure:

#### Initial Application Structure
```
src/main/java
 |
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

### Data Structures and Algorithms
For this artifact I have chosen the [Zoo Monitoring Command Line Interface (CLI)](https://github.com/paronicholas/ZooMonitorSystem), a Java based application, which I first developed in the IT 145: Foundations in Application Development course at Southern New Hampshire Univeristy.

### Database
