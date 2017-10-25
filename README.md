# Summer_Experience_Explorer
Iteration 3 Implementation Summary and Instructions
Jacob, Oliver, Pietro, Nick


Proper Display of Database Table in basic GUI via swing table model:
Jacob and Pietro solved a bug that was causing the data values from the database to display in an incorrect order. Fixed the problem and now a basic GUI displays exactly what was entered into the database (in this case our excel.csv file). 
Finalization of enhanced GUI that displays a database table/has the ability to filter data from the database: 
Nick finalized a really unique GUI that is easy to use and is visually attractive. Jacob/Nick then connected the code to this enhanced GUI to display the database table within it via a swing table model. Oliver applied the code that filtered the data to the users preference. 
Connect/Create (if not already created) to the database and database table when running the main class of the program, not by running a seperate class with a seperate main method.
Jacob modified previous code to connect/create (if not already created) a database and database table when running the main class of the program. The program previously accomplished this by running a separate class with its own main method.

User Stories: Year Filter, State Filter, City Filter, Industry Filter, Work Hours Filter, Payment Filter, Search Button, User Story:
Oliver, through the creation of the filterDB method in the ExperienceFilter class, filtered the ArrayList of all Experiences to include only Experiences that matched the user criteria. The user criteria was compared, one by one, to the characteristics of the Experience, and if the Experience was found to not match, the Experience was filtered out. A challenge was encountered as the last value in the table contained an extra space, therefore giving an unexpected value in comparison with the user criteria. Pietro helped solve this problem by using the trim() method to remove the blank space, and coding a JUnit test for it. We wanted to visibly see this criteria filter database entries, and managed to do this in under one iteration. 

User Stories (a couple more filters): Internship Filter, International Filter (formerly Visa Filter):
These filters had a slightly different implementation in the filtration process, since they were selected by the user as checkboxes. Oliver and Nick worked to capture this variability, and ensure the creation of a functioning Criteria object, checked-box or not. This is relevant to a sizeable percentage of the student body that might have different circumstances and the career center as a potential stakeholder that also needs to provide their services to international students.

User Story: Restore Previous Search:
Nick implemented a command pattern to encapsulate the search functionality of the program and implemented an undo method that restores the previous search criteria and search result to the gui. This user story has a clear and testable endpoint, which improves the user experience and overall would improve the potential of our application. 

User Story: Reset Search Criteria:
Nick added a button that, when pressed, resets the search criteria back to starting prompt values and restores the full table to the GUI, this was an example of user stories that were broken down in order to have a clear endpoint and attain specific deliverables throughout our iterations.

User Story: Change Color Scheme:
Nick implemented a ColorScheme strategy pattern and added a button that, when pressed, changes the GUI’s attribute colorScheme to a new instance of a concrete ColorScheme class. The color scheme changes in a rotation of three schemes with the press of the “Change Color Scheme” button, which makes the project maintainable and reduces the potential cost of having to change color if Colorado College decides do rebrand with different colors in the future, adding business/marketing value. 

User Story: Criteria Class
Oliver created a Criteria class to aid the filtering of the Experience ArrayList.This was in response to instructor feedback. The Criteria class stores the user selections of filters as Strings and then compares them to the characteristics of Experiences in the ArrayList. This is very measurable as showcased on the unit tests, and appeals to all different user types, the employee end and the customer end in the career center exchange services. Moreover, as developers we wanted to maximize the scope parameter within our fixed parameters.

Instructions
				
Use MAMP to start the Apache and MySQL servers that will support the database
Make sure the port is set to match that of the code in the “createDatabase.java” file (8889). 
Import Iteration 3 into eclipse. Make sure the “states.txt.” and “Summer expereince survey 2016 for oliver.csv” files are in the project folder
Left click project folder and select Build Path, then Configure Build Path.
Remove the .jar sql file that is marked as an error. 
Right click the java project > then select  “add external archives.”
Add your “mysql-connector-java-5.1.44-bin.jar.” file to ensure a connection to the database.
Run Project (DbQuery contains main method).
 

Database Connection/Creation Side Note 
The code delivered to you should have a properly created database that doesn't allow table duplication due to our usage of a singleton method. If you would like to check the functionality of the createDatabase class/creation of the database you will need to first drop the database that we have already created. This can be done by selecting the “experiences” database > selecting the “operations” tab > and then selecting  “drop the database (DROP).” The program can still be run normally but will now create a new database instead of simply checking to see if the database has already been properly created. 





