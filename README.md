# Part4-Exercise3




## A)

#### `challange1`

**Language Features**
- Inheritance and Polymorphism: The challenge1 method takes a parameter of type Bird which is an abstract class that implements two interfaces Winged and Bipedal, meaning that any subclass of Bird such as Crow, inherits the default methods fly() from Winged and walk() from Bipedal. This feature also demonstrates polymorphism due to the ability to use a single interface (Bird) to represent different subclasses (Crow), allowing method calls like b.fly() and b.walk().

**How does this feature manifest?**
- The challenge1 method explicitly requires an object of type Bird or its subclass, which inherently has the fly() and walk() methods becasue of the interfaces that Bird implements. Therefore, it can only accept instances of Bird or its subclasses, even if another unrelated class implements both Winged and Bipedal.


**How should it be used?**
- When the method is intended to work strictly with a class hierarchy, and additional shared behaviors or properties from the abstract class (Bird) are required.


#### `challange2`

**Language Features**
- Generics: The method challenge2 uses generics with multiple bounds which means that the type X must implement both the Winged and Bipedal interfaces.

**How does this feature manifest?**
- The generic constraint <X extends Winged & Bipedal> allows any class that implements both interfaces to be passed, not just subclasses of Bird which provides flexibility since it isn't limited to a specific class hierarchy.


**How should it be used?**
- When you want to allow flexibility by accepting any type that satisfies certain interface contracts.
