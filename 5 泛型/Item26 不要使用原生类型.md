# Item26 不要使用原生类型

Item26 不要使用原生类型

> First, a few terms. A class or interface whose declaration has one or more _type parameters_ is a _generic_ class or interface \[JLS, 8.1.2, 9.1.2]. For example, the List interface has a single type parameter, E, representing its element type. The full name of the interface is List (read “list of E”), but people often call it List for short. Generic classes and interfaces are collectively known as _generic types_.

首先介绍一些使用到的术语，一个类或者接口，如果它的声明中带有一个或者多个类型参数，那么它就是要一个泛型类或接口 \[JLS, 8.1.2, 9.1.2]。比如，List接口就有一个类型参数E，用来表示其中元素的类型。这个接口的全称是List（读作E的列表），人们通常将其简称为List。泛型类和接口也被统称为泛型。

> Each generic type defines a set of _parameterized types_, which consist of the class or interface name followed by an angle-bracketed list of _actual type parameters_ corresponding to the generic type’s formal type parameters \[JLS, 4.4, 4.5]. For example, List (read “list of string”) is a parameterized type representing a list whose elements are of type String. (String is the actual type parameter corresponding to the formal type parameter E.)

每一个泛型都包括一组参数类型，其构成方式如下：首先是类或者接口的名字，然后紧跟着用<>括起来的实际类型参数，实际类型参数和泛型中的形式类型参数对应。比如List（读作String的列表），就是一个表示列表的元素类型为String的参数类型，其中String就是一个对应形式类型参数E的实际类型参数。

> Finally, each generic type defines a _raw type_, which is the name of the generic type used without any accompanying type parameters \[JLS, 4.8]. For example, the raw type corresponding to List is List. Raw types behave as if all of the generic type information were erased from the type declaration. They exist primarily for compatibility with pre-generics code.

最后，每个泛型类型都定义了一个原生类型，其名字就是没有任何类型参数的泛型类型的名称。比如List的原生类型就是List。原生类型就像是把类型信息从类型声明中擦除了样。它们存在的主要目的是为了保持泛型出现之前的代码的兼容性。

> Before generics were added to Java, this would have been an exemplary collection declaration. As of Java 9, it is still legal, but far from exemplary:

在泛型被加入到Java中之前，下面这段集合声明是可以说是值得参考的。在Java9中，这段代码也是合法的，但却没什么参考价值了。

```java
// Raw collection type - don't do this!
// My stamp collection. Contains only Stamp instances.
private final Collection stamps = ... ;
```

> If you use this declaration today and then accidentally put a coin into your stamp collection, the erroneous insertion compiles and runs without error (though the compiler does emit a vague warning):

如果你现在使用这样的声明，然后不小心往stamp集合里插入了一个coin，这个错误的插入可以正常的编译和运行（虽然编译器会报一个模糊的警告）。

```java
// Erroneous insertion of coin into stamp collection
stamps.add(new Coin( ... )); // Emits "unchecked call" warning
```

> You don’t get an error until you try to retrieve the coin from the stamp collection:

直到你要从stamp集合里取出这个coin的时候，才会报错。

```java
// Raw iterator type - don't do this!
for (Iterator i = stamps.iterator(); i.hasNext(); )
Stamp stamp = (Stamp) i.next(); // Throws ClassCastException stamp.cancel();
```

> As mentioned throughout this book, it pays to discover errors as soon as possible after they are made, ideally at compile time. In this case, you don’t discover the error until runtime, long after it has happened, and in code that may be distant from the code containing the error. Once you see the ClassCastException, you have to search through the codebase looking for the method invocation that put the coin into the stamp collection. The compiler can’t help you, because it can’t understand the comment that says, “Contains only Stamp instances.”
>
> With generics, the type declaration contains the information, not the comment:

正如这本书中经常提到的那样，在错误出现后，应该尽快发现，最好是在编译期发现。在这个例子中，要在运行时才能发现错误，而且错误发生了很久了才会报错，报错的代码和实际出错的代码相隔很远。一旦你看见了ClassCastException，你就必须要搜索所有的代码来找到把coin放入stamp集合的方法调用。编译器帮不了你，因为它不能理解“只包含Stamp实例”这个注解。

使用泛型的话，这个类型声明就会包含这个信息，而不是写注解里。如下：

```java
// Parameterized collection type - typesafe
private final Collection<Stamp> stamps = ... ;
```

> From this declaration, the compiler knows that stamps should contain only Stamp instances and _guarantees_ it to be true, assuming your entire codebase compiles without emitting (or suppressing; see Item 27) any warnings. When stamps is declared with a parameterized type declaration, the erroneous insertion generates a compile-time error message that tells you _exactly_ what is wrong:

从这个声明中，假设你的整个代码库在编译器都没有抛出（或者隐藏，详见Item27）任何警告，编译器就可以知道stamps只应该包含Stamp实例，并且做出保证。当stamp列表使用参数类型声明的时候，错误的插入在编译器就会生成一个错误信息，告诉你哪里出错了：

```java
Test.java:9: error: incompatible types: Coin cannot be converted to Stamp
       c.add(new Coin());
                 ^
```

> The compiler inserts invisible casts for you when retrieving elements from collections and guarantees that they won’t fail (assuming, again, that all of your code did not generate or suppress any compiler warnings). While the prospect of accidentally inserting a coin into a stamp collection may appear far-fetched, the problem is real. For example, it is easy to imagine putting a BigInteger into a collection that is supposed to contain only BigDecimal instances.

当从集合中取出元素的时候，编译器会进行隐式地转换，并保证不会失败（同样地，其前提还是，你的所有的代码在编译时没有生成或隐藏任何的警告）。虽然不小心把一个coin插入到stamp集合中，有点牵强，但是这类问题却是真实存在的。比如，就很容易想象，有人会把BigInteger插入到只支持BigDecimal实例的集合中去。

> As noted earlier, it is legal to use raw types (generic types without their type parameters), but you should never do it. **If you use raw types, you lose all the safety and expressiveness benefits of generics.** Given that you shouldn’t use them, why did the language designers permit raw types in the first place? For compatibility. Java was about to enter its second decade when generics were added, and there was an enormous amount of code in existence that did not use generics. It was deemed critical that all of this code remain legal and interoperate with newer code that does use generics. It had to be legal to pass instances of parameterized types to methods that were designed for use with raw types, and vice versa. This requirement, known as _migration compatibility_, drove the decisions to support raw types and to implement generics using _erasure_ (Item 28).

正如前面说的那样，虽然使用原生类型是合法的，但是你永远都不应该这样做。\*\*如果你使用了原生类型，你就失去了泛型带来的安全性和所有的描述性方面的优势。\*\*既然我们不应该用它们，那为什么语言的设计者还要允许使用它们呢？是为了保持兼容性。当泛型加入的时候，Java即将进入它的第二个十年，已经有大量的没有使用泛型的代码存在了。保证已经存在的代码合法，并且可以和使用泛型的代码互相调用，这是很重要。而且将参数化类型的实例传递给为原生类型设计的方法必须是合法的。这个要求，称为“移植兼容性”，促成了支持原生类型和使用擦除来实现泛型的决定（Item28）。

> While you shouldn’t use raw types such as List, it is fine to use types that are parameterized to allow insertion of arbitrary objects, such as List. Just what is the difference between the raw type List and the parameterized type List? Loosely speaking, the former has opted out of the generic type system, while the latter has explicitly told the compiler that it is capable of holding objects of any type. While you can pass a List to a parameter of type List, you can’t pass it to a parameter of type List. There are subtyping rules for generics, and List is a subtype of the raw type List, but not of the parameterized type List (Item 28). As a consequence, **you lose type safety if you use a raw type such as** **List, but not if you use a param- eterized type such as List.**
