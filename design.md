
# Design Document
![Architecture for TaskMaster](https://alenrtan.github.io/amaa-team.github.io/TaskMaster_Architecture.png)

## Architecture
- The AMAA team has decided to use a repository-style architecture with slight 
features from the architectural style of layering. 
The team chose this architecture due to it's simple way of showing how different methods can connect the frontend to the backend. Furthermore, it helps visulize the relationship from top to bottom of the software.

- When TaskMaster is first started, the user is greeted with the frontend, which contains all the buttons that they are allowed to press. 
    - At the same time, the backend access the storage for the project, a `.csv` file.

- Whenever a user presses a button (or enters text(s) to a field) (grey objects on the diagram), this directly calls a method and helps do what the user wants to do.

- In the backend, `Storage`, `Store Reminder`, and `Load Reminder`, work closely with one another; as both Store Reminder and Load Reminder depend on storage. For `Flush Reminders`, this depends on `Load Reminder`. <br>

## Major Classes and Object Responsibilites
- Currently there are three important classes:
    - `TaskMaster_Main.java`
        - The main job of this class is to setup the environment properly (loading the correct welcome screen, loading the correct application icon, .css file, etc.). Once all of the needed setup portions have been done, all control relinquishes to `Controller.java`

    - `TaskMaster_Reminders.java`
        - Working hand-in-hand with `Controller.java`, this class has all the needed methods to store, load, and access reminders. It will also contain the methods for quotes.
        - This class is also responsible for checking and accessing the `.csv` file, where all the reminders are stored.
        - see ["Object Responsibilities"](https://alenrtan.github.io/amaa-team.github.io/design.html#Object-Responsibilities)

    - `Controller.java`
        - Once control has been relinquished from `TaskMaster_Main.java`, the controller class contains methods for each button and text field the user may use/fill out. The class works directly with the `.fxml` files found in the project folder.
    
- FXML Files
    - All files with the `.fxml` extension contain the necessary data for the frontend, essentially. They contain what each button will do (using the `Controller.java` class) and which method said button will do.

- Object Responsibilities
    - The `Controller.java` class creates a `TaskMaster_Reminders` object. The purpose of creating this object is for storage purposes. The `storeReminders()` method takes a list as a parameter. The creation of the object helps with this, as there is a global list that contains `TaskMaster_Reminders` objects, which are then stored one-by-one in the .csv file.

