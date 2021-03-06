# 1. Cover

##Orientation game: Requirements of the system

| Product Name        | Orientation game         |
|---------------------|--------------------------|
| Team name           | EVAN                     |                         
| Team members        | Eder Jiménez O’Shanahan  |
|                     | Veronika Pepoeva         |
|                     | Alejandro Rueda Pérez    |
|                     | Natalija Kuzova          |
| Date of the report  | 4.12.2013                |
| Editors             | Eder Jiménez O’Shanahan  |
|                     | Veronika Pepoeva         |
|                     | Alejandro Rueda Pérez    | 
|                     | Natalija Kuzova          |


# 2. Introduction

<br>
### Motivation 

<p>Every year there are new students coming to the university and in order to participate in the Metropolia's activities it is important to know the school's facilities: computer rooms, auditoriums, laboratories, libraries, gym, cafeteria etc. The area of the university is rather big and it can be quite complicated for the newcomers to orientate at first. 

<p>We came up with the idea that instead of regular guided tour around the campus during the orientation week we can create an interactive game for the students. This game will not only help to get familiar with the university area but also will demonstrate and advertise the opportunities of today’s media technologies.

<p>The main idea to involve all team members of the group is to log in to the same team views from different smart phones and to use different tools (views) at the same time.
In overall the game will create much more interactive way to present the university facilities to the new students and demonstrate the technological side of the studying process in Metropolia.

### Game description

<p>The game is implemented as a mobile application. The students are divided into groups of 3 to 5 people.The goal of each team is to get first through all the checkpoints around the campus.
<p>Main idea of the game:
* Each team gets a group name and password from the tutor as soon as the teams are formed
* By login under same name and password team members get same destinations list
* The checkpoint is scored when the QR code is scanned in the required destination
* When the QR code is scanned the team gets a check mark next to the destination name in the list.
* The first team who gets all the checkpoints tagged wins 
<p>Main features of the game:
* Direction list: In order to find the destination player has to follow given directions. The list of directions and metric distances from point to point appears as soon as the destination has been chosen. 
* Compass tool: In order to complicate the task directions are given in cardinal and ordinal format and players has to use compass to follow them. 
* Radar tool: The tool is created so that the teams can interact with each other. Radar will show if there are other team players around as soon as the tool is opened, but at the same time it will uncover the position of the team. Tool allows placing a mine or a compass bomb that can slow down other teams on their way. Also it allows to see the same obstacles on their way. 
           <p> * Mine: It is possible to place a mine in the current position. The penalty for "stepping" on the mine is 5 mins extra time for the total team time result.
           <p> * Compass Bomb: It is possible to place a compass bomb in the current position. If the player steps on the compass bomb, the compasses of the team will stop showing right cardinal directions during next 5 min.

In order to involve some strategic thinking each team has limited amount of mines and bombs they can use.
Each of the described tools is provided on the separate view and the idea is that each team member can be in charge of different tool. This will help to have everyone in the team involved in the process. 




# 3. Use Cases
## 3.1 Definition of the user groups

| User group                 | Brief definition          | Definition                                            |
|----------------------------|---------------------------|-------------------------------------------------------|
| Tutor                      | Manager of the game       | The tutor is able to start the game,                  |
|                            |                           | so that every student (user) could start playing at   |
|                            |                           | the same time. Administrator owns the data with all   |
|                            |                           | the team names and passwords.                         |
| Student                    | Logged in user (Player)   | Student has to log in before the game is started.     |
|                            |                           | Player is using all the features of the game. Player  |
|                            |                           | is collaborating with his team members and interacts  |
|                            |                           | with other teams                                      |


## 3.2 Use case diagrams
![first](UseCase Diagram0.jpg)
## 3.3 Use case scenarios

## Use case scenarios

### Log In
* Actors: Tutor, Student
* Preconditions: 
* Initial state: The user is in the log in screen.
* Normal flow:
  1. The user enters the team name and password.
  2. The user presses the "Log in" button.
  3. If the credentials are correct, the user is logged in to the system.
  4. For the student, the waiting screen will appear. For the tutor, the tutor screen will appear.
* What can go wrong: 
  + The user forgot/lost the password.
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
* End state: The user is waiting for the game to start.

### Start game
* Actors: Tutor
* Preconditions: 
  1. The user is logged in.
* Initial state: The user is in the tutor screen.
* Normal flow:
  1. The tutor presses the "Start game" button.
  2. The game starts.
  3. Every student of the game gets a notification. Now all the students automatically access the homescreen.
* What can go wrong: 
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
* End state: The game has began.

### Scan QR code
* Actors: Student
* Preconditions: 
  1. The user is logged in.
  2. The game has been started by the tutor.
* Initial state: The user is in the homescreen.
* Normal flow:
  1. The user has found the QR sticker and is ready to scan it.
  2. The user presses the "QR" button and the QR scanner opens.
  3. The user centers the QR code inside the guides shown with the camera.
  4. The QR code is recognized and the QR scanner closes, the user is back to the homescreen.
  5. A verification tick is placed beside the checkpoint that has now been verified.
* What can go wrong: 
  + The QR code is incorrect, the user is scanning an invalid QR code for the selected checkpoint: The QR scanner closes and the checkpoint doesn't get verified.
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
  + All the team members get the verification tick for the checkpoint.
* End state: The checkpoint has been verified and the team is now able to select the next checkpoint they want to search.

### Select active checkpoint
* Actors: Student
* Preconditions: 
  1. The user is logged in.
  2. The game has been started by the tutor.
* Initial state: The user is in the homescreen.
* Normal flow:
  1. The user taps the checkpoint that the team wants to find.
  2. The checkpoint is now active and the button appears to be pressed.
* What can go wrong: 
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
  + The active checkpoint is updated and synchronized to all of the team members.
  + Now the active checkpoint cannot be changed until one of the team members successfully scans the QR code.
  + Directions are updated:
    1. Right after the checkpoint is marked as active, the directions to reach it from the actual coordinates are calculated.
    2. These directions are updated and available now under the "Directions" tab.
* End state: The checkpoint is marked as active and now the team can start searching it.

### Place a mine
* Actors: Student
* Preconditions: 
  1. The user is logged in.
  2. The game has been started by the tutor.
* Initial state: The user is in the home screen.  
* Normal flow:
  1. The user opens the radar screen by pressing the "Radar" tab.
  2. Press the button: "Place Mine".
  3. A mine is placed in the current coordinates of the user.
* What can go wrong: 
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
  + The mine is updated to the system and now available to every player in the game.
* End state: The mine is successfully placed and shown in the radar.

### List directions for active checkpoint
* Actors: Student
* Preconditions: 
  1. The user is logged in.
  2. The game has been started by the tutor.
* Initial state: The user is in the home screen.  
* Normal flow:
  1. The user presses the tab "Directions".
  2. The directions to reach the active checkpoint are shown in a list form.
* What can go wrong: 
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
* End state: The user can see the directions to reach the active checkpoint.

### See enemies
* Actors: Student
* Preconditions: 
  1. The user is logged in.
  2. The game has been started by the tutor.
* Initial state: The user is in the home screen.  
* Normal flow:
  1. The user opens the radar screen by pressing the "Radar" tab.
  2. The nearby enemies are shown in the radar as red dots.
* What can go wrong: 
  + The user loses the internet connection.
  + The user receives a phone call.
  + The phone runs out of battery.
* Other activities going on at the same time:
* End state: The user is in the radar screen seeing in real time where the enemies are.

## 3.4 Descripction of one use case as a flow chart
![my hyper flowchart](Place Mine diagram.png)

# 4. System Arquitecture
Our game is divided in 3 subsystems which are needed for the correct behaviour 
of the whole game. In the following image are represented those three subsystems
and how they cooperate between them. 
+  Authentication system: Is in charge of checking if the credentials are correct
and communicating the main engine of the game in which user group is a certain user, so that
which roles he has. 
+  Main Engine: The main engine is in charge of the logic of the game and to communicate
with the Authentication system and the Storage System. 
+  Storage System: Is in charge of receiving requests from the main engine, process them and
access to the DB to return the appropriate answer.


![system](Systems.PNG)

# 5. Requirements

## 5.1 Functional Requirements

* Student can login as a group member
* Student can start activities only when the game is started by the tutor
* Student can see list of directions only for the chosen point of destination 
* Student renews the directions view by choosing other destination
* Student gets a point when QR code scanned
* Student is able to navigate between the views apart of the team
* Student is able to see enemies on the radar only if enemies are also in the radar mode
* Student gets extra 5 min to the total time if steps on the mine
* Student is able to place a mine at the current position if not already exist
* Student is able to place a compass bomb at the current position if not already exist
* Student is not able to use the compass if stepped on the compass bomb
* Student reviles his position when in the radar mode
* Position of the student is hidden if not in the radar mode
* Ranking of the teams updates during activation of the view
* The timer stops when all QR codes are scanned


## 5.2 Non-functional system requirements
 
###Usability:

To ensure that the system is easy to use, 
there was made a research while trying to imagine the game only looking at the user interface. After that was decided to remove some buttons.

It was decided to make tabs for easy navigation. Every member of the team will manage with his own tab, 
so it makes the game easier (if every player had to use all the functions of the game by himself at the same time  there would be much mess). Any actions needs no more than 3 clicks.

There are no useless buttons or much unnecessary information. The program is light and easy-to-understand. 

The front page will allow the player to log in. After that it will be possible to choose a
checkpoint and follow the instructions. All the instructions are brief and non-complicated. 
The game requires to be attentive and to be able to use a smartphone.

###Reliability:
              
Before starting the game every player has to log in. If the login or password are not correct the system will ask to log in again. Noone can start playing until the Tutor has started the game. This makes the game honest, so that all the players could start playing at the same time and there was no false start. 

All the information will be stored in the secure place and protected.

Possible system failures can be:
+ Incorrect Username/Password --> log in again

###Efficiency: 
             
System has to be able to work with a lot of people at the same time. The most crucial requirement for the system is to update immediately, so that the information about checkpoints, mines and compass bombs was availiable for other players at the same time.
The system is efficient if the response time is fast. 

The game has to work with all the Operating Systems (Android, IOS, Windows, Firefox, etc.)

###Response time:

The time that system takes to react to a given input has to be very small. Because the game is multi-player and real-time it is crutial that the information updated in no more then 2 seconds time and does not stop other processes of the game.

###Other non-functional requirements:

To avoid unambiguity and misunderstanding there are used different colors (suitable for color-blind) for identification. On radar screen the color of the mines, compass bombs and other players have to vary from each other.  All the buttons also have to distinguish by color.


# 6. User Interface

### Menu Screen 
This is how main menu looks. It is divided in 
two zones: 
+  The first zone is where the user can see the main checkpoints buttons that is necessary to reach to finish
the game, the QR button, the time the user has been playing and the Ranking Button.
  * Checkpoints buttons: pressing those buttons the user selects the checkpoint that 
	he wants to download the information to the Direction Screen.
  * QR: This button is needed to be activated when the user finds the checkpoint paper with the QR code in it.
  * Ranking: This button allows the user to check in which position his group is compared to the other groups.
+  The second zone is the footer bar menu where the user can change the view of the first zone.
When a sucessful scan is done, a verification tick will appear next to the active checpoint button.

![Menu](Menu.PNG)

Menu Screen Just after the Waiting Screen.

![Menu2](Menu2.PNG)

Menu Screen after 54 minutes 
	
### Directions Screen
This is how directions screen looks. There is the footer bar menu as in the Menu Screen and in the main view
there is a list with the directions and the number of meters to reach each point of the selected checkpoint.
	
![Directions](Directions.PNG)

Directions Screen

### Compass Screen
This is how directions screen looks. There is the footer bar menu as in the Menu Screen and in the main view
there is a compass.
![Compass](Compass.PNG)

Compass Screen

### Radar Screen
This is how directions screen looks. There is the footer bar menu as in the Menu Screen and in the main view
there is a Radar where appears the enemies, the mines and the bombs. There are also two buttons:
+ The "Place Mine" button: the user place the mine in his current position.
+ The "Place Compass Bomb" button: the user place the mine in his current position.
![Radar](Capture.PNG)

Radar Screen

 
# 7. Project management

One of the most time consuming part was the idea creation itself. In order for us to separate the work load each team member had to have a clear vision of the game structure, its flow and main functionalities. We had 2 brainstorming sessions: one during the lab and one outside of class. This sessions allowed as to describe the idea fully.

We also had to set the boundaries according to the time limitations we had. Some of the ideas we excluded or simplified due to the fact that we did not have time to describe them fully. They were left for the possible of further development.

Since each team member had a good image how the final product should look like it was easy to separate the work between us and contribute to the work of each other. It was separated who responsible for documenting each part of the requirements, but in fact all the ideas were discussed within the group since we were implementing the project together in the school.

####Responsibilities division:

•	Eder Jiménez O’Shanahan: Use Cases, Team management

•	Veronika Pepoeva: Introduction, Requirements, Project Management description

•	Alejandro Rueda Pérez: User Interface, System Architecture

•	Natalija Kuzova: Requirements, Use cases.

####Realized working hours:

* Each team member personal time contribution: 8 h(2 labs that were fully dedicated to this document and approximately 2 hours outside of the class)
* Brainstorming sessions: 2 h
* Total dedicated time for the project: 34 hours


We were a bit limited by the fact that we do not have experience in implementation of this type of projects yet, so we are not familiar with all the processes and skills needed. Due to this fact we probably could not predict every aspect of this project.

We found it a bit difficult to find the optimal way to describe the functionalities and structure of our application, since the examples of similar documentation were quite different from each other and not always good. There were not many standards or templates how to describe our requirements or system architecture that we could follow. It was more about which way we consider more logical in our case.
 
In overall we consider our product successful. It has an interesting idea behind and a useful purpose. At the same time it is well described and is possible to be implemented. As with every project there are sure could be done some modifications, but at this stage we are satisfied with the result we came up with.


