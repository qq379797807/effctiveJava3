# 5 泛型

> **S**INCE Java 5, generics have been a part of the language. Before generics, you had to cast every object you read from a collection. If someone accidentally inserted an object of the wrong type, casts could fail at runtime. With generics, you tell the compiler what types of objects are permitted in each collection. The compiler inserts casts for you automatically and tells you _at compile time_ if you try to insert an object of the wrong type. This results in programs that are both safer and clearer, but these benefits, which are not limited to collections, come at a price. This chapter tells you how to maximize the benefits and minimize the complications.

从Java5开始，泛型就成为了Java语言中的一部分。在拥有泛型之前，你必须对每个从集合中读出来的对象进行类型转换。如果有人不小心插入了一个错误类型的对象，这个类型转换就会再运行时失败。使用泛型，你就可以告诉编译器，那些类型的对象允许加入这个集合。编译器会自动地为你进行转换，然后当你要插入一个错误类型的时候，在编译地时候就会报错。这样会使得程序更加安全和清晰，但是要享有这些好处（不仅仅限于集合），是有一定的代价的。本章将告诉你如何将这些好处最大化，同时降低复杂度。
