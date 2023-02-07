Mariah Carey can impressively sing up to 5 out of 8 octaves. Why does she have such a wide vocal range? Because of her inheritance. Queen Mimi’s mom is an opera singer and a vocal coach.

In programming, Inheritance is one of the key concepts of Object Oriented Programming (OOP). It allows an object to be based on another object, which is useful when different objects are similar and share some common logic, but they are not identical. Inheritance sustains code reusability by allowing an object to reuse the code of another object while it adds its own logic as well.

So, in order to achieve inheritance, we reuse the common logic and extract the unique logic in another class. This is known as an IS-A relationship, a.k.a parent-child relationship. It’s just like saying Foo IS-A Buzz type of thing. Eg., puma IS-A feline, and motorcycle IS-A vehicle. An IS-A relationship is the unit of work used to define hierarchies of classes.

In Java, inheritance is accomplished via the extends keyword by deriving the child from its parent.
And in Python, a reference to the superclass is passed as a parameter into the subclass.

The child can reuse the fields and methods of its parent and add its own fields and methods. The inherited object is called the superclass, or the parent class. The object that inherits the superclass is called the the subclass, or the child class.

In Java, inheritance cannot be multiple. Hence, a subclass cannot inherit fields and methods of more than one superclass.

Unlike Java, Python supports multiple inheritance. The ability of a class to inherit more than one class is called Multiple Inheritance. Using multiple Inheritance, a subclass can have multiple superclasses. super() is a function that returns a temporary representation of a parent class.

    class A:
       def target(self):
       print("Invoked method in class A")

    class B(A):
       def target(self):
           print("Invoked method in class B")
           super().target()

    class C(A):
       def target(self):
           print("Invoked method in class C")
           super().target()

    class D(B, C):
       def target(self):
           print("Invoked method in class D")
           super().target()
    obj = D()
    obj.target()

Output:

    Invoked method in class D
    Invoked method in class B
    Invoked method in class C
    Invoked method in class A
