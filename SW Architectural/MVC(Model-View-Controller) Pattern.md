MVC(Model-View-Controller) Pattern is one of software design pattern. It is a software design pattern that emerged to divide user interface logic and business processing logic.
# MVC Structure
MVC is divide `Model`, `View`, `Controller`. 
![](https://www.freecodecamp.org/news/content/images/2021/04/MVC3.png)           
## Model
Model's major role is superintending data. Examples of things that require data processing, such as api, database value change, logic processing, etc., are all done by model. 

In conclusion, Model performs task processing logic, and mainly manages data.
## Controller
Controller is a part that most in contact with users. The controller's responsibility is to pull, modify, and provide data to the user. Essentially, the controller is the link between the view and model.

In conclusion, controller is managing flows between view models and even manage the overall flow of MVC behavior.
## View
View's role is to show users. And, view decide what the user will see on their screen.

In conclusion, view is based on the data of the model received from the controller, the view is selected to show the view.

---
Reference link 🙂           
https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller            
https://www.freecodecamp.org/news/the-model-view-controller-pattern-mvc-architecture-and-frameworks-explained/