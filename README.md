# GreenPlate
Introduction

GreenPlate is an app that allows individuals to track their eating and shopping habits, in order to promote sustainability and a healthy lifestyle. Through GreenPlate, users have the ability to keep track of calorie intake, find new recipes, manage ingredients, and create shopping lists. The data visualization functionality empowers individuals to understand their dietary habits with an intuitive interface. Further, users can create their own accounts to interact with the interface in a secure and reliable manner. This comprehensive project was implemented across the course of four sprints, each introducing additional functionality to provide users with the best experience possible! Keep scrolling to learn a little bit more about the various aspects of our project, including the design & architecture, user interface (UI), functionality, and some reflections looking back on the past semester.

Design & Architecture

Throughout the course of this project, we utilized various Unified Modeling Language (UML) diagrams to visualize the functionality of our project in an intuitive way. Two primary UML diagrams we utilized were Sequence Diagrams (SD) and Design Class Diagrams (DCD). As we navigated the creation of the app, we periodically outlined specific use cases with a lot of moving parts and developed the design framework to simplify the software development process for these instances. Below are some examples of this method in action!

Sequence Diagram (SD)

User Case: If the user enters valid ingredient information and hits the submit button, the system will store this ingredient to their pantry and it will be displayed on the ingredient screen.


![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/2d0d74a8-8daa-4d63-940b-1b39ae846769)

Figure 1. Existing user adds valid ingredient to pantry properly

Design Class Diagram (DCD)

User Case: An existing Greenplate user logs into the app and attempts to add an ingredient to their pantry. This opens the form entry for adding an ingredient. The user enters the ingredient information and clicks the button to submit the new ingredient. They are directed back to the ingredient page after clicking the back button. There the new ingredient is displayed in the ingredient list.


![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/d8134098-eeaa-4647-96f3-d462ffc34cb0)

Figure 2. Diagram for all the classes required to add new ingredient/recipe

In addition to UML diagrams, we also made use of SOLID/GRASP design principles to ensure that our code was maintainable and reuseable throughout the course of the project. Below, we have outlined a few examples of our use of these principles, and included a brief explanation outlining their purpose in the context of our project.

SOLID

Single Responsibility: The Ingredient class in our code represents Single Responsibility in SOLID. This class wholly represents an ingredient and everything connected with it. This class only has one job, which is to represent an instance of an ingredient and everything within this class is used to get data from the ingredient or set data within the ingredient.

Interface Segregation: The SortStrategy interface in our code demonstrates the Interface Segregation Principle (ISP) from the SOLID principles of object-oriented design. This interface is used in our Strategy Pattern, every class that implements it needs to have the sortList method because the implementations are algorithms for sorting recipeList. In the Strategy Pattern, each class implementing the SortStrategy interface focuses solely on providing a sorting algorithm for the sortList method, adhering to the Interface Segregation Principle by avoiding the inclusion of unrelated methods. This approach promotes flexibility and allows clients to switch between different sorting strategies seamlessly without being tied to unnecessary interface methods.

GRASP

Information Expert: The Recipe class exemplifies the Information Expert principle of GRASP. The Recipe class has the necessary information pertaining to recipes, and as a result it contains information pertaining to ingredients, which in turn makes it uniquely qualified to update a field such as the ingredient list. It is because of this that the Recipe class is most qualified to fulfill the responsibility of managing recipes and ingredient lists for users.

High Cohesion: High Cohesion in GRASP (General Responsibility Assignment Software Patterns) is a design principle that requires that the methods and attributes in a class are closely related and work toward achieving a clear and focused purpose. In this class, all of the methods and attributes are related to the concept of a user profile. Methods like setEmail, setWeight, setHeight, and setGender are responsible for setting user attributes. Conversely, methods like getEmail, getWeight, getHeight, and getGender are responsible for retrieving user attributes. The getInstance method ensures that only one instance of the User class is created, which utilizes the Singleton design pattern.

Creator: The User class exemplifies the creator principle by incorporating the Singleton pattern. This design ensures that only the User class can instantiate user objects and guarantees that there exists only one instance. The User class assumes this responsibility because it is best suited to manage its own instantiation and lifecycle.

User Interface

In our app, we had five main screens: Ingredient List, Recipe, Meal Information, Shopping List, and User Info. Let's take a visual tour of each of these screens before we dive into the key functionality!

Ingredient List

Functionality: This page displays the user's pantry inventory, allowing them to add, update, or remove ingredients as needed for meal preparation and shopping planning.

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/201bcdfd-345c-4ae3-b620-f2b91cfdba30)

Recipe

Functionality: Users can access and create recipes here, seeing ingredient availability based on their pantry inventory. They can also interact with the shopping list feature to add missing ingredients for recipes.

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/dae9ba2f-9ebe-4ffc-9702-9b0bc848c408)

Meal Information

Functionality: This page covers logging meals, tracking calorie intake, and setting personalized calorie goals based on user-specific information like height, weight, and gender.

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/29215aa3-4f7c-4b71-b0a2-ceef25d21168)

Shopping List

Functionality: Here, users can view and manage their shopping lists, which may include automatically suggested items based on recipe ingredients not in the pantry, as well as manual additions and deletions.

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/560e3edf-02f1-433c-bead-fad63012c576)

User Info

Functionality: This page manages user authentication, account creation, and storage of personal information used for personalized features within the app, ensuring a secure and tailored experience for each user.

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/acdc2280-b13e-42fe-adac-66dd218e1d93)

Functionality

[Insert Video Here]

Conclusions and Reflections/Learning

Looking back on this semester, we've come to appreciate the multitude of skills we've developed in such a short span. Before this term, none of us had any exposure to Android Studio or Firebase. However, as the semester unfolded, we grew increasingly confident in using these tools. Beyond just meeting the functional coding requirements outlined in the project specifications, we delved into various industry-relevant software development principles and design patterns, such as SOLID/GRASP and the Strategy pattern. As we look ahead to further education or our careers in the industry, we're assured of our ability to apply these learnings in meaningful ways.

One of the most valuable aspects of this journey has been our collaborative experiences. While we've engaged in many group project-based courses and will continue to do so, this course stood out due to its similarity to real-world industry collaboration. We embraced Agile methodologies, crafted JIRA dashboards, and scheduled regular Scrum meetings, mirroring industry practices. We extend our gratitude to Dr. Nimisha Roy and the entire CS 2340 teaching team for their unwavering support throughout this semester!

Collaborators: Kaushik Sriram, Nick Ginac, Ben Hellman, Abi Saravanakumar, Andrew Luo
