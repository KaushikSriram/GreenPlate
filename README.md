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

Functionality: User can add/remove ingredients from their shopping list

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/201bcdfd-345c-4ae3-b620-f2b91cfdba30)

Recipe

Functionality: Users can add recipes to their recipe list, and sort the list on the basis of Name and Calorie Total

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/dae9ba2f-9ebe-4ffc-9702-9b0bc848c408)

Meal

Functionality: Users can enter meals/calories to generate intuitive graphs to visualize their meal data

![image](https://github.com/KaushikSriram/GreenPlate/assets/154042167/29215aa3-4f7c-4b71-b0a2-ceef25d21168)


