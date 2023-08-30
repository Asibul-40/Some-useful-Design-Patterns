
# Creational Pattern:
Creational design patterns are strongly concerned with the way of creating any object. These patterns are designed for reducing complexities and the way of reusing the code in a different manner in terms of creating an object. <br/>
Some mentionable creational design patterns are: 
- *Factory method pattern*
- *Builder pattern*. 

## Builder pattern:
- Used to build a complex object in a particular sequencing manner.
- Used to produce different types with different representation of an object using the same construction code.
- Creates the complex object by separating out the instantiation process of the object.

Let's visualize an example: <br/>

![Untitled Diagram (28)](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/07fba960-55d4-4e00-b87b-bacc1e4b131f)


Suppose, we have made a new house with some pre-defined properties, like: *houseType*, *totalWindows*, *totalDoors* etc. What if one of our clients wants a different types of house with some new additional properties, like: *totalFloor*, *hasGarage* etc. We can simply solove this problem by using inheritance and by defining these attributes into the class constructor.
But what is the gurantee that our client will not ask another new type of house with some other properties ?
- By using inheritance, we can have multiple categories of houses with all kinds of *house requirements* combination. This will increase the hierarchy quite a lot.
- If we define the properties to the constructors, the for every new requirements we need to change our constructor with the additional properties, which violates the *open-close principle*.

![Untitled Diagram (30)](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/df7cb762-636a-4801-8b8d-d9533396c60a)


