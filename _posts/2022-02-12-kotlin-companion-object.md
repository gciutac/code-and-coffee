---
layout: post
title: 'Kotlin Companion Object'
subtitle: Create Static Methods and Properties
cover-img: /assets/img/companion-object-header.png
thumbnail-img: /assets/img/lamda.jpeg
share-img: /assets/img/companion-object.png
tags: [Kotlin, companion object]
---

In Kotlin, the `companion object` is a powerful feature that allows you to define static properties and methods within a class. In this article, we'll explore what a companion object is, how it works, and some examples of how it can be used in Kotlin.

**What is a Companion Object?**

A companion object is a special object that is tied to a class, rather than an instance of the class. It allows you to define static properties and methods that can be accessed without creating an instance of the class.

In Kotlin, the `companion object` keyword is used to define a companion object. Here's an example:

```
class MyClass {
    companion object {
        val staticProperty = "Hello, world!"

        fun staticMethod() {
            println("Static method called!")
        }
    }
}
```

Here, the `MyClass` class defines a companion object using the `companion object` keyword. The companion object has a static property called `staticProperty`, which is a string, and a static method called `staticMethod()`, which prints a message to the console.

**How do Companion Objects Work?**

When you define a companion object, it is created at the same time as the class, and it can be accessed using the class name. For example, you can access the static property and method of the `MyClass` companion object like this:

```
println(MyClass.staticProperty) // prints "Hello, world!"
MyClass.staticMethod() // prints "Static method called!"
```

Here, we access the `staticProperty` and `staticMethod()` of the `MyClass` companion object using the class name, rather than an instance of the class.

**Companion Objects and Factory Methods**

One of the most common uses of companion objects in Kotlin is for creating factory methods. A factory method is a method that creates and returns instances of a class, rather than using the constructor directly.

Here's an example of a factory method defined in a companion object:

```
class Person private constructor(val name: String) {
    companion object {
        fun create(name: String): Person {
            return Person(name)
        }
    }
}
```

Here, the `Person` class has a private constructor, which means that instances of the class can only be created from within the class. The `Person` class also has a companion object with a factory method called `create()`, which creates and returns a new instance of the `Person` class.

By defining the `create()` factory method in the companion object, we can create new instances of the `Person` class without needing to call the constructor directly. Here's an example:

```
val person = Person.create("John")
println(person.name) // prints "John"
```

Here, we create a new `Person` instance using the `create()` factory method defined in the `companion object`, and we access the `name` property of the `Person` instance.

**Conclusion**

Companion objects are a powerful feature of Kotlin that allow you to define static properties and methods within a class. They are commonly used for creating factory methods, as well as for defining static properties and methods that can be accessed without creating an instance of the class. By using companion objects, you can write more expressive and concise code that is easier to read and maintain.
