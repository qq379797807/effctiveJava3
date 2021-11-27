# 3 对所有的对象都通用的方法

> **A**LTHOUGH Object is a concrete class, it is designed primarily for extension. All of its nonfinal methods (equals, hashCode, toString, clone, and finalize) have explicit _general contracts_ because they are designed to be overridden. It is the responsibility of any class overriding these methods to obey their general contracts; failure to do so will prevent other classes that depend on the contracts (such as HashMap and HashSet) from functioning properly in conjunction with the class.
>
> This chapter tells you when and how to override the nonfinal Object methods. The finalize method is omitted from this chapter because it was discussed in Item 8. While not an Object method, Comparable.compareTo is discussed in this chapter because it has a similar character.

虽然Object是一个具体的类，但是这个类就是设计来扩展的。为了更好的被覆盖（overridden），它的所有非final的方法（equals, hashCode, toString, clone, 和 finalize）都有明确的通用约定（general contract）。任何类要覆盖这些方法的时候，都有责任遵守这些通用约定。否则这些类将无法和基于这个约定时限的类（不如HashMap和HashSet）一起正常的运作。

本章告诉你什么时候以及如何去覆盖Object的非final方法。其中finalize方法并不在本章中讨论，因为Item8里面已经讨论过了。虽然Comparable.compareTo不是Object的方法，但由于它有类似的特征，所以本章中也对它进行了讨论。
