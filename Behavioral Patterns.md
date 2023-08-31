
# Behavioral Patterns

Behavioral design patterns are concerned with algorithms and the assignments of responsibilities between objects. Basically, these patterns deal how objects are interacting with each other. Such type of patterns are:
- Observer pattern
- Strategy pattern

## Observer Pattern
- Follows one-to-many relationships pattern between objects and all the dependent objects are notified whenever the state of the *Observable(Subject)* object changes.
- Objects interacts with each other by following the broadcast-type communication.
- This pattern ensures *loosely coupling* between the concrete subject and the observers. As the concrete subject only know one thing: any observer need to implement a certain interface to become the subject's observer.
- We can add or remove any observer at runtime.

This is the overall architecture of the observer pattern:

![observer-pattern-arch](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/ff3cafde-b622-488a-ba71-db7186c59fdc)

- **Subject:** The necessary abstract class or interface where the necessary operations (*add*, *remove*, *notify*) are defined for the observers to the subject.
- **Concrete Subject:** It maintains the state of data and also notifies all its observers whenever the state changes.
- **Observer:**  The necessary concrete operations to notify all observers.
- **Concrete Observer:** Implements the *notified* method of the concrete observer interface.

Let's dive into an example: <br/>
We often play games in our freetime. Suppose, the Gaming authority has decided to annouce some updating patch to all their gaming users. One way is to sent the updated news to the gamers one-by-one. But is this the effective & efficient solution to spread their updated content ? 

![Untitled Diagram (36)](https://github.com/Asibul-40/Some-useful-Design-Patterns/assets/77221075/3c1c4f68-97f5-4dd1-8aab-0410ff4c36ba)

We can solve such type of situation by using the observer pattern.
- **GameUpdateNews:** The context or data that will be passed to all the gamers whenever it changes.
- **GamingSubject:** The interface or abstract class where all the required concrerte method are defined for the gamers to gaming authority.
- **GamingAuthority:** Whenever the state of the *gameUpdateNews* changes, the gaming authority notifies all the game users.
- **GamingContent:** The required concrete methods are defined to spread the news to all gamers. And all the gamer class needs to implement the method to get that updated news.
