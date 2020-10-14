## Professional Self-Assessment

## Informal Code Review

## Artifacts
### Software Engineering and Design
For this artifact I have chosen the [Zoo Monitoring Command Line Interface (CLI)](https://github.com/paronicholas/ZooMonitorSystem), a Java based application, which I first developed in the IT 145: Foundations in Application Development course at Southern New Hampshire Univeristy. I chose this application because it provided the best opportunity for improvement within a completed application and offered a change for me to showcase areas of growth with regards to my utilization and understanding of software engineering and design principles. For this portion of improvements, I focused on re-designing the structure of the application to better follow object-oriented design principles and class based structures. The re-design also incorperated my learning of test-driven development and secure coding principles.

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

### Data Structures and Algorithms
For this artifact I have chosen the [Zoo Monitoring Command Line Interface (CLI)](https://github.com/paronicholas/ZooMonitorSystem), a Java based application, which I first developed in the IT 145: Foundations in Application Development course at Southern New Hampshire Univeristy. I chose this application for the data structures and algorithms improvement for similar reasons to the software engineering and design segment - the Zoo Monitoring CLI offered the best opportunity to showcase my areas of improvement in data structure and algorithmic implementation. For this refactor I mainly focused on the `Parse.java` class. In the initial implementation of this class, the Parse class read was called every time a monitor was chosen. The parsing method - `monitorInfoParser` would loop through a list of strings, retrieved from the specified text file, and then remove everything prior to the expected animal or habitat.
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
This implementation did not offer any error handling or provide any reliability in the system if a user input the incorrect information into the text file. For the refactor, I extracted out the different portions of this method into helper functions and used the new `Animal` and `Habitat` objects created in the software engineering and design refactor to dynamically build a list of `Animal` or `Habitat` objects to be used for the chosen monitor menu. This refactor allowed me to add in additional error handling, ensure that all `Animal` or `Habitat` objects had the same structures, and improved the overall efficiency by reducing the number of times the text files needed to be parsed while the system was running. The new structure, and stack tracing, can be followed from the [`buildAnimalList`](https://github.com/paronicholas/ZooMonitorSystem/blob/master/src/main/java/helper/Parse.java#L71) method or the [`buildHabitatList`](https://github.com/paronicholas/ZooMonitorSystem/blob/master/src/main/java/helper/Parse.java#L97) method.

### Database
