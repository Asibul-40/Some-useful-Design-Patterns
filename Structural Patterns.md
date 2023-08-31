# Structural Design Pattern
Structural design patterns are a blueprint of how different objects & classes are combined together to form a bigger structure. These patterns focus on how the classes and objects are composed with each other so that they become replacable as solutions. <br/>
Some mentionable such patterns are:
- Facade pattern
- Decorator pattern

## Facade Pattern
The term *facade* means to have a artificial or false apprearance of an object. This pattern can be simply defined as: providing a simple interface to communicate for any complex set of objects.
- *Hides the complexity* of a subsystem, means **decouples** a client from the subsystem components.
- Provides a *simpler view* to shuild the user from knowing the complex details of the system.
- This pattern still leaves the subsystem accessible, which can directly be used to add new functionalities.

The simplified structure of facade pattern:

![facadeDemoStructure](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/ba0907f6-2209-4c16-b3a0-1922a06ebe9a)


> Image source: [Refactoring Guru](https://refactoring.guru/design-patterns/facade)

- **Facade:** Provides a simplified interface to interact the subsystem components. The client directly use this interface to get the system's services.
- **Additional Facade:** The additional facade can communicate both client and other facades and hence prevents the single facade to get polluted from unnecessary attributes.
- **Complex Subsystem:** The internal functional componenets of a system. They communicate with each other to perform some specific tasks and they have no idea about what the facade component does.
- **Client**: Use the facade instead of calling the subsystem modules.

Consider the following example:

![Untitled Diagram (32)](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/9dc0ec93-610a-4737-a877-dbe682017d48)

Let's say, we have a computer and we want to do some tasks using this computer. For this, we need to start our computer from its power-off state. So we are only concerned about opening our computer by tapping the *power button*. We don't know how our computer will start to operate with its internal components, like: *processor*, *ram*, *operating system* etc. 
- **CPU, Memory, OS (Complex subsytem):** The internal functional modules of a computer. To start a computer, these modules are needed to be setup their functionality fro the *executable* state. Hence, these complex functionalities are always hidden from a normal user.
- **FacadeComputer:** The simplified interface to operate a computer properly without having the knowledge of *how computer is performing its functional tasks*.
- **User:** The users interacts with the *FacadeComputer* interface to get the services.

## Usecases of Facade Pattern
- We should use this pattern when there needs a common middleware to communicate with some internal complex architectures.
- To design some layering approach for the subsystem, we can use some facade to interact with those layers. 

