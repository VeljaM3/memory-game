# Memory Game

A simple memory card game built with HTML and JavaScript.

The project employs functional programming principles through its use of an Entity-Component-System (ECS) architecture, pure functions, and a focus on data transformation. Below is an explanation of how functional programming is applied in this project:

**Entity-Component-System (ECS) Architecture**  
The project is structured around an ECS pattern, commonly used in game development, which aligns well with functional programming concepts:

* **Entities**: Each card in the game is represented as an entity, an object that holds a collection of components. Entities are created with a constructor (Entity) and have methods like addComponent to associate components with them. Each entity has a unique ID to distinguish it.
* **Components**: These are simple objects with a name and a value, representing properties like position (x, y), value (card value), flipped (whether the card is face-up), and matched (whether the card has been paired). While ideally components would be immutable in a functional approach, this code modifies their values in place (e.g., e.components.flipped.value = true).
* **Systems**: These are functions that operate on the entities array to implement game logic. The project includes two main systems: userInputSystem and renderingSystem.
