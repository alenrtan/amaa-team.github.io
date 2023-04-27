# Test Report

1. Component Testing
    - Processing User Input and Storage
        - Processing the user input involved many different steps in order for it to work properly - writing the correct data to the .csv file. Before being able to fully integrate the user input from the front end to the back end, we had many "dummy" files to experiment with different processing, such as:
            - Creating a new `TaskMaster_Reminders` object every single time and proceeding to add this object to a list, then call the `StoreReminders()` method with the list as a parameter. In theory, this would work, as this did not create any errors and actually saved to the file. However, when it came to creating multiple reminders, the previous reminders would be listed multiple times (duplicates)
            - Creating new `TaskMaster_Reminders` object and directly using this as the parameter for `StoreReminders()`. This would only work if the user would input **one** reminder **per** session - which is not always the case!
            - Using a global list that is accessible to both `Controller.java` and `TaskMaster_Reminders` classes and continuously appending to the end of the list whenever the user creates a new reminder. The list will then traversed by `StoreReminders()` and will store each object, one object per line. This helped solve the problem of not being able to create multiple reminders per session and the problem of duplicates! 
        - Using the third option, we were confident enough to integrate it to the main program and it worked as planned.
        - Test Data included:
            1. Duplicate reminder names
            2. Duplciate reminder names + description + dates
            3. Multiple reminders 
        - Tested through many iterations of self-input.

2. System Testing
    - Testing the system as a whole was fairly simple throughout. After running the program, the tests pretty much followed the same order throughout every iteration:
        1. Test if the program launches correctly 
            - Is it the right screen?
            - Checking the terminal, are there any null pointer exeptions?
            - Does the window/any on-screen material look off?
                - This was a common cause of wrong scaling on the front end (fixed!)
        2. Test every button
            - Did it change screens? If not, check `Controller.java`
            - Check the back button
                - Is it back to the welcome screen?
        3. Test functionality
            - Create:
                - Make different reminders - some the same title and date
            - Delete:
                - Delete a reminder, go back, select `show all`
            - Show all:
                - Does it show all reminders?
                    - if not, proceed to step 4. Otherwise, testing complete.
        4. Test Back end:
            - check `reminders.csv`
            - check for null `TaskMaster_Reminders` list
                - check if object creation is correct (is it the right constructor?) 

3. Acceptance Testing
    - The requirements of the user were simple and therefore the acceptance testing shall be simple as well; acceptance was determined through testing the program through a third-person perspective. There was also a time were I had a non-group member try the program. Furthermore, a criteria was deemed successful if the critera was easily done through the program.
    - Activity reminders
        - Accepted; mostly implemented
    - Motivational Quotes
        - Not accepted; no implementation
    - Graphical User Interface
        - Accepted; completely implemented
    - Minimal User Interface
        - Accepted; completely implemented
        








