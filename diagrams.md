# A collection of useful diagrams that may aide in softare design

1. **MVC Architecture diagram**

MVC is an architeactural pattern/framework that separates application into 3 main logical componenets, serving to break down complicated development process into more manageable pieces.
This also separates the backend implementation logic/business logic from the frontend visual display. 
- controller: the 'middleman' between view and model, acting as a brain that receives request and send response back to the client. 
- view: handles how data is representated and the visual display (UI logic) -- only interacts with controller
- model: handles all data related logic, which is either the data that is being transferred between the View and Controller components or any other business logic-related data. Responsible for retrieving data from DB.

Sources/Readings:
- https://youtu.be/mtZdybMV4Bw
- https://youtu.be/pCvZtjoRq1I
- https://www.geeksforgeeks.org/mvc-framework-introduction/
- https://www.freecodecamp.org/news/the-model-view-controller-pattern-mvc-architecture-and-frameworks-explained/
- https://www.codecademy.com/article/mvc

2. **Sequence Diagram (UML)**

Sequence diagram models the interactions between objects in a single use case. (how different parts of the application works together to get a sequence done)
Unified Modelling Language (UML) is a modeling language in the field of software engineering which aims to set standard ways to visualize the design of a system.
Depiction of the sequence of events is in sequential order, handling all the logic that flows from the start to the end of the event.

Source/Readings:
- https://creately.com/guides/sequence-diagram-tutorial/#what-is-a-sequence-diagram
- https://www.geeksforgeeks.org/unified-modeling-language-uml-sequence-diagrams/
- https://www.youtube.com/watch?v=pCK6prSq8aw

3. **ERD (Entity Relation Diagram)**


The most useful diagram for modelling database tables and their relationships for relational database in my opinion. It is is a type of flowchart that illustrates how “entities” such as people, objects or concepts relate to each other within a system.
Good for relational DB design and debugging. They mirror grammatical structure, with entities as nouns and relationships as verbs.

Source/Readings:
- https://www.youtube.com/watch?v=QpdhBUYk7Kk&t=96s
- https://www.youtube.com/watch?v=-CuY5ADwn24
- https://www.lucidchart.com/pages/er-diagrams

4. **Class diagrams (UML)**

Class diagrams model its classes, attributes, operations, and relationships between objects. It facilitates OOP principles. Useful to document software architecture, class diagrams are a type of structure diagram because they describe what must be present in the system being modeled
Consists of a few componenets such as access modifiers, scopes... 

Source/Readings:
- https://www.geeksforgeeks.org/unified-modeling-language-uml-class-diagrams/
- https://www.lucidchart.com/pages/uml-class-diagram
- https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-class-diagram/
