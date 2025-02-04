# Part4-Exercise3




## A)

#### `challange1`

**Language Features**
- Inheritance and Polymorphism: The challenge1 method takes a parameter of type Bird which is an abstract class that implements two interfaces Winged and Bipedal, meaning that any subclass of Bird such as Crow, inherits the default methods fly() from Winged and walk() from Bipedal. This feature also demonstrates polymorphism due to the ability to use a single interface (Bird) to represent different subclasses (Crow) which allows method calls like b.fly() and b.walk().

**How does this feature manifest?**
- The challenge1 method explicitly requires an object of type Bird or its subclass, which inherently has the fly() and walk() methods becasue of the interfaces that Bird implements. Therefore, it can only accept instances of Bird or its subclasses.

**How should it be used?**
- When the method is intended to work strictly with a class hierarchy and additional shared behaviors or properties from the abstract class (Bird) are required.


#### `challange2`

**Language Features**
- Generics: The method challenge2 uses generics with multiple bounds which means that the type X must implement both the Winged and Bipedal interfaces.

**How does this feature manifest?**
- The generic constraint <X extends Winged & Bipedal> allows any class that implements both interfaces to be passed, not just subclasses of Bird which provides flexibility since it isn't limited to a specific class hierarchy.


**How should it be used?**
- When you want to allow flexibility by accepting any type that satisfies certain interface contracts regardless of their position in the class hierarchy.




## B)

#### Functional Differences

1. Type constraints and flexibility:
   - `challenge1(Bird b)`: This method only accepts an object of type Bird or its subclasses. Therefore, if you have another class (unrelated to Bird) that implements Winged and Bipedal, you cannot pass it to challenge1, even if it has the required fly() and walk() methods.
   - `challenge2<X extends Winged & Bipedal>(X b)`: This method accepts any type that implements both Winged and Bipedal regardless of whether it belongs to the Bird class hierarchy.

2. Extensibility and Reusability:
   - `challenge1`: This method is tightly coupled to the Bird class hierarchy. If you want to extend this functionality to non-bird objects that can fly and walk, you would need to modify the method or create new ones.
   - `challenge2`: The use of generics makes this method more reusable. It can work with any object that fits the interface requirements (Winged and Bipedal), not just birds.

3. Method signature differences:
   - `challenge1`: The method signature is based on a concrete class (Bird). This approach uses inheritance and polymorphism but limits the method to objects of that specific type.
   - `challenge2`: The method signature uses generics with multiple bounds which makes the method more abstract and adaptable, focusing on behavior rather than type.
  

## C)

The advantage of `challenge2` is its flexibility and reusability. By using generics with multiple bounds, `challenge2` allows any object that implements both interfaces, regardless of its class hierarchy, to be passed into the method. So now, let's imagine we are building a simulation for a zoo that contains animals and machines like drones that can fly and walk. While birds like Crow, are natural candidates, we may also have machines like Drones that have similar behavior but don’t belong to the Bird class hierarchy. With `challenge2`, we can handle both animals and machines as long as they implement the Winged and Bipedal interfaces. 

   






















