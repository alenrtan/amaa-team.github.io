


# Requirements Specification for Project AMAA
--------------------------------------- 

### <br>1.1 Purpose of Product<br>
The purpose of this productivity application is to help people store and keep track of tasks set by the user of the program. 
We plan to accomplish this by allowing the users to set custom tasks that the application will store and organize for the user. 
We hope this will help the user have an easier time to keep track of important tasks or events. 
The application will also encourage the user to complete their tasks by giving motivational quotes based on how successful they are at completing them. 
We plan to make this program a beneficial addition to people’s planning process so they can accomplish more and be more efficient with their time.

### <br>1.2 Scope of Product<br>
The main purpose of the application is to help a user be able to achieve his or her daily goals and by having it all in one place the user can constantly have an idea of how well their day is going. The main problem we are trying to tackle is the frequency with which people are unable to simply complete the things they set out to complete at the start of the day.
The application is not an instant fix or a remedy, but it is the best possible way to keep our users accountable to themselves, and that is what we aim at doing with our app. 
The application provides the user with an interface where he/she can setup their daily goals and the app will provide timely reminders and also provide them with a completion rating at the end of the day, followed by a motivational quote that will be chosen on the basis of their completion rating.

### <br>1.3 Acronyms, Abbreviations, Definitions<br>
+ Wherever “we” is mentioned, it is defined as the group as the whole and what decisions the group has made. Specific information from specific people will be implicitly noted.
+ For outside sources and other information regarding outside information, please see the ["References"](https://alenrtan.github.io/amaa-team.github.io/problem.html#references) portion.<br><br>

+ *Definitions*:
  + AMAA 
    + Alen, Marco, Alex, Anish
    + The first initials of the names of members in the group.
  + Application
    + A format; Desktop-based application
  + JavaFX
    + The library that we will be using in order to implement the GUI portion of the project. We will use the built-in functions that will help create the window, and objects in the window, that the user can interact with.
  + TaskManager
    + The name of the application. TaskMaster is made by AMAA Team.

### <br>1.4 References<br>
+ **Project Site:** [Learn more about our project!](https://alenrtan.github.io/amaa-team.github.io/)
+ **Program Repository:** [Check out the nitty gritty details of our code!](https://github.com/aacuna45/AMAA-Project)
+ **Project Site Repository:** [Behind the scenes of our page!](https://github.com/alenrtan/amaa-team.github.io)
+ **JavaFX Website:** [This is the resource we plan to use to make our program look great!](https://openjfx.io/)

### <br> 2.1 Context of Product <br>
- Our project will be a desktop program that runs locally on the user's computer/laptop.

### <br>2.2 Domain Model with Description<br>
![Domain Model for TaskMaster](https://alenrtan.github.io/amaa-team.github.io/DomainModel.png) <br>
The domain model above is a general representation of the TaskMaster application. The TaskMaster application relies on the 3 different major parts: 
  1. User
  2. Controller
  3. Reminders

The user represents the most "top-level" in the hierarchy. The user has access to the other relative sections, as the user is where the information comes from. Once there is information to store, user input, then it will be sent to the Controller class `controller.java` <br>

The controller class is what handles the buttons and forms that the user can interact with. It is the bridge between the user and the c<?
Storage and reminders work hand-in-hand. Whenever the controller receives input, it is sent to be process by the reminders class. This, then, is stored in the reminders.

On-time reminders is how the user can see how often they are finishing tasks on time.

### <br>2.3 Product Functions (general)<br>
- The Taskmaster program will have functionality for the user to add tasks to a list which the program will keep track of. The program will remind users to complete tasks, and will additionally provide encouragement through offering motivational quotes along with the reminders.

### <br>2.4 User Characteristics and Expectations<br>
- Our userbase will want organized tasks with added reminders to encourage them to complete these tasks. TaskMaster users only need the most basic computer skills, ability to use a mouse to click on things, and keyboard to type. Users will need to read text in our program to select the correct functions they want and to know what information(s) needs to be input.

### <br>2.5 Constraints<br>
- Our program currently has the constraint of only running on devices that have successfully installed JavaFX/OpenFX. This is due to the needed dependencies. [See 2.6.](https://alenrtan.github.io/amaa-team.github.io/requirements.html#26-assumptions-and-dependencies)
  
  - This issue is currently being researched on.

### <br>2.6 Assumptions and Dependencies<br>
- The TaskMaster program depends heavily on the many `.jar` files provided by the [OpenFX software](https://openjfx.io/).
- For the time being, it is the assumed that the user has Java 17+ and some JavaFX version 17+ installed.

### <br>3. Functional Requirements<br>
- Please see: [User Stories](https://alenrtan.github.io/amaa-team.github.io/userstories.html)

### <br>4.1 External Interface Requirements (User,Hardware, Software, Communications)<br>
- Our program will have a GUI that comes up in a window on the computer screen. There is interaction with the user using a keyboard and mouse to select functions and enter information into the program, which may occur on overlays in our window.
- NF.4.1.1 
  - Device must have a display
- NF.4.1.2 
  - Devcice must have mouse input
- NF.4.1.3 
  - Device must have keyboar input

### <br>4.2 Performance Requirements<br>
- The Taskmaster program will be low-impact with regards with performance and will not require many system resources.
<br>
  - NF.4.2.1 
    - Resource efficient to run with other programs 
<br>
  - NF.4.2.2 
    - Run on a Windows system (Other OS options are not being planned)
<br>
  - NF.4.2.3 
    - Be storage efficient for data storge

### <br>4.3 Design Constraints<br>
The Taskmaster program is designed to be a simple java application to keep track of the information given by the user. The only data that can be accessed is the files within its folder.  
<br>
  - NF.4.3.1 
    - The program will only store the data given by the user in reminders and completion record 
<br>
  - NF.4.3.2 
    - The program will be offline only and save data locally 
<br>
  - NF.4.3.3 
    - The program will be accessed through a GUI 
<br>
  - NF.4.3.4 
    - All processes will executed through the application 

### <br>4.4 Quality Requirements <br>
- Our users need the program to not have any glitches and be reliable to remind them of tasks at the correct times. Being simple to use and easy to learn is also important to make it appeal to many users.
<br>
  - NF.4.4.1 
    - Aesthetic Visual Design that does not strain the eyes.
  <br>
  - NF.4.4.2 
    - Basic GUI with only the required buttons for functions (clutter-free).
  <br>
  - NF.4.4.3 
    - Continuous reminders at appropriate times until tasks are marked as complete by user.

### <br>4.5 Other Requirements<br>
- NF.4.5.1 
  - Taskmaster must be simple to use, it is a one size fits all application.
<br>
- NF.4.5.2 
  - Must help users realiably track their usage of time.
<br>
- NF.4.5.3 
  - Quotes and notifications must not flood the users desktop and become counter-productive. 

### <br>5. Appendices<br>
- [Usage of JavaFX / OpenFX documentation can be found here](https://openjfx.io/openjfx-docs/).
<br> 
- Additional user constraints specified in the [user stories](https://alenrtan.github.io/amaa-team.github.io/userstories.html).
