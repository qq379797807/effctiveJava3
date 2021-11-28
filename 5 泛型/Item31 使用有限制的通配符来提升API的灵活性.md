# Item31 使用有限制的通配符来提升API的灵活性

> As noted in Item 28, parameterized types are _invariant_. In other words, for any two distinct types Type1 and Type2, List is neither a subtype nor a supertype of List. Although it is counterintuitive that List is not a subtype of List, it really does make sense. You can put any object into a List, but you can put only strings into a List. Since a List can’t do everything a List can, it isn’t a subtype (by the Liskov substitution principal, Item 10).
