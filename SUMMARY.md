# Table of contents

* [effctiveJava第三版-中英对照自翻译](README.md)
* [2 创建和销毁对象](2-chuang-jian-he-xiao-hui-dui-xiang/README.md)
  * [2 创建和销毁对象](<2 创建和销毁对象/Item1 考虑使用静态方法替代构造器.md>)
  * [Item2 当构造器有多个参数时，可以考虑使用Builder](2-chuang-jian-he-xiao-hui-dui-xiang/item2-dang-gou-zao-qi-you-duo-ge-can-shu-shi-ke-yi-kao-lv-shi-yong-builder.md)
  * [Item3 使用私有构造器或枚举类型来强化单例](2-chuang-jian-he-xiao-hui-dui-xiang/item3-shi-yong-si-you-gou-zao-qi-huo-mei-ju-lei-xing-lai-qiang-hua-dan-li.md)
  * [Item4 通过私有构造器强化不可实例化的能力](2-chuang-jian-he-xiao-hui-dui-xiang/item4-tong-guo-si-you-gou-zao-qi-qiang-hua-bu-ke-shi-li-hua-de-neng-li.md)
  * [Item5 优先考虑依赖注入来引用资源](2-chuang-jian-he-xiao-hui-dui-xiang/item5-you-xian-kao-lv-yi-lai-zhu-ru-lai-yin-yong-zi-yuan.md)
  * [Item6 避免创建不必要的对象](2-chuang-jian-he-xiao-hui-dui-xiang/item6-bi-mian-chuang-jian-bu-bi-yao-de-dui-xiang.md)
  * [Item7 清除过期的对象引用](2-chuang-jian-he-xiao-hui-dui-xiang/item7-qing-chu-guo-qi-de-dui-xiang-yin-yong.md)
  * [Item8 避免使用终结方法和清除方法](2-chuang-jian-he-xiao-hui-dui-xiang/item8-bi-mian-shi-yong-zhong-jie-fang-fa-he-qing-chu-fang-fa.md)
  * [Item9 try-with-resources 优先于try-finally](2-chuang-jian-he-xiao-hui-dui-xiang/item9-trywithresources-you-xian-yu-tryfinally.md)
* [10 异常](10-yi-chang/README.md)
  * [10 异常](<10 异常/Item69 只针对异常的情况使用异常.md>)
* [10 异常](10-yi-chang-1/README.md)
  * [Item70 对于可以恢复的情况使用受检异常，编程错误使用运行时异常](<10 异常/Item70 对于可以恢复的情况使用受检异常，编程错误使用运行时异常.md>)
* [10 异常](10-yi-chang-2/README.md)
  * [Item71 避免受检异常的不必要的使用](<10 异常/Item71 避免受检异常的不必要的使用.md>)
* [10 异常](10-yi-chang-3/README.md)
  * [Item72 优先使用标准的异常](<10 异常/Item72 优先使用标准的异常.md>)
* [10 异常](10-yi-chang-4/README.md)
  * [Item73 抛出和抽象对应的异常](<10 异常/Item73 抛出和抽象对应的异常.md>)
* [10 异常](10-yi-chang-5/README.md)
  * [Item74 为每个方法抛出的所有异常建立文档](<10 异常/Item74 为每个方法抛出的所有异常建立文档.md>)
* [10 异常](10-yi-chang-6/README.md)
  * [Item75 在细节信息中包含失败-捕获信息](<10 异常/Item75 在细节信息中包含失败-捕获信息.md>)
* [10 异常](10-yi-chang-7/README.md)
  * [Item76 努力保持失败的原子性](<10 异常/Item76 努力保持失败的原子性.md>)
* [10 异常](10-yi-chang-8/README.md)
  * [Item77 不要忽略异常](<10 异常/Item77 不要忽略异常.md>)
* [3 对所有的对象都通用的方法](3-dui-suo-you-de-dui-xiang-du-tong-yong-de-fang-fa/README.md)
  * [3 对所有的对象都通用的方法](<3 对所有的对象都通用的方法/Item10 覆盖equals时请遵守通用规则.md>)
* [3 对所有的对象都通用的方法](3-dui-suo-you-de-dui-xiang-du-tong-yong-de-fang-fa-1/README.md)
  * [Item11 覆盖equals时总是要覆盖hashCode](<3 对所有的对象都通用的方法/Item11 覆盖equals时总是要覆盖hashCode.md>)
* [3 对所有的对象都通用的方法](3-dui-suo-you-de-dui-xiang-du-tong-yong-de-fang-fa-2/README.md)
  * [Item12 始终要覆盖toString](<3 对所有的对象都通用的方法/Item12 始终要覆盖toString.md>)
* [3 对所有的对象都通用的方法](3-dui-suo-you-de-dui-xiang-du-tong-yong-de-fang-fa-3/README.md)
  * [Item13 谨慎地覆盖clone](<3 对所有的对象都通用的方法/Item13 谨慎地覆盖clone.md>)
* [3 对所有的对象都通用的方法](3-dui-suo-you-de-dui-xiang-du-tong-yong-de-fang-fa-4/README.md)
  * [Item14 考虑实现Comparable接口](<3 对所有的对象都通用的方法/Item14 考虑实现Comparable接口.md>)
* [4 类和接口](4-lei-he-jie-kou/README.md)
  * [4 类和接口](<4 类和接口/Item15 最小化类和成员的可访问性.md>)
* [4 类和接口](4-lei-he-jie-kou-1/README.md)
  * [Item16 在公有类中使用访问方法，而不是公有域](<4 类和接口/Item16 在公有类中使用访问方法，而不是公有域.md>)
* [4 类和接口](4-lei-he-jie-kou-2/README.md)
  * [Item17 使可变性最小化](<4 类和接口/Item17 使可变性最小化.md>)
* [4 类和接口](4-lei-he-jie-kou-3/README.md)
  * [Item18 组合优先于继承](<4 类和接口/Item18 组合优先于继承.md>)
* [4 类和接口](4-lei-he-jie-kou-4/README.md)
  * [Item19 要么专门设计继承并提供文档，要么禁止继承](<4 类和接口/Item19 要么专门设计继承并提供文档，要么禁止继承.md>)
* [4 类和接口](4-lei-he-jie-kou-5/README.md)
  * [Item20 接口优先于抽象类](<4 类和接口/Item20 接口优先于抽象类.md>)
* [4 类和接口](4-lei-he-jie-kou-6/README.md)
  * [Item21 为后代设计接口](<4 类和接口/Item21 为后代设计接口.md>)
* [4 类和接口](4-lei-he-jie-kou-7/README.md)
  * [Item22 接口只用来定义类型](<4 类和接口/Item22 接口只用来定义类型.md>)
* [4 类和接口](4-lei-he-jie-kou-8/README.md)
  * [Item23 类层次优于标签类](<4 类和接口/Item23 类层次优于标签类.md>)
* [4 类和接口](4-lei-he-jie-kou-9/README.md)
  * [Item24 静态成员类由于非静态成员类](<4 类和接口/Item24 静态成员类由于非静态成员类.md>)
* [4 类和接口](4-lei-he-jie-kou-10/README.md)
  * [Item25 限制源文件为单个顶级类](<4 类和接口/Item25 限制源文件为单个顶级类.md>)
* [5 泛型](5-fan-xing/README.md)
  * [5 泛型](<5 泛型/Item26 不要使用原生类型.md>)
* [5 泛型](5-fan-xing-1/README.md)
  * [Item27 消除非受检的警告](<5 泛型/Item27 消除非受检的警告.md>)
* [5 泛型](5-fan-xing-2/README.md)
  * [Item28 列表优先于数组](<5 泛型/Item28 列表优先于数组.md>)
* [5 泛型](5-fan-xing-3/README.md)
  * [Item29 优先考虑泛型](<5 泛型/Item29 优先考虑泛型.md>)
* [5 泛型](5-fan-xing-4/README.md)
  * [Item30 优先考虑泛型方法](<5 泛型/Item30 优先考虑泛型方法.md>)
* [5 泛型](5-fan-xing-5/README.md)
  * [Item31 使用有限制的通配符来提升API的灵活性](<5 泛型/Item31 使用有限制的通配符来提升API的灵活性.md>)
* [5 泛型](5-fan-xing-6/README.md)
  * [Item32 谨慎地并用泛型和可变参数](<5 泛型/Item32 谨慎地并用泛型和可变参数.md>)
* [5 泛型](5-fan-xing-7/README.md)
  * [Item33 考虑类型安全的异构容器](<5 泛型/Item33 考虑类型安全的异构容器.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie/README.md)
  * [6 枚举和注解](<6 枚举和注解/Item34 使用枚举代替int常量.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-1/README.md)
  * [Item35 用实例代替序数](<6 枚举和注解/Item35 用实例代替序数.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-2/README.md)
  * [Item36 用EnumSet代替位域](<6 枚举和注解/Item36 用EnumSet代替位域.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-3/README.md)
  * [Item37 使用EnumMap代替序数索引](<6 枚举和注解/Item37 使用 EnumMap代替序数索引.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-4/README.md)
  * [Item38 用接口模拟可以扩展的枚举](<6 枚举和注解/Item38 用接口模拟可以扩展的枚举.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-5/README.md)
  * [Item39 注解优先于命名模式](<6 枚举和注解/Item39 注解优先于命名模式.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-6/README.md)
  * [Item40 坚持使用Override注解](<6 枚举和注解/Item40 坚持使用Override注解.md>)
* [6 枚举和注解](6-mei-ju-he-zhu-jie-7/README.md)
  * [Item41 用标记接口定义类型](<6 枚举和注解/Item41 用标记接口定义类型.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream/README.md)
  * [7 Lambda和Stream](<7 Lambda 和 Stream/Item42 Lambda优先于匿名类.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-1/README.md)
  * [Item43 方法引用优于lambdas](<7 Lambda 和 Stream/Item43 方法引用优于lambdas.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-2/README.md)
  * [Item44 优先使用标准的函数接口](<7 Lambda 和 Stream/Item44 优先使用标准的函数接口.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-3/README.md)
  * [Item45 谨慎地使用Stream](<7 Lambda 和 Stream/Item45 谨慎地使用Stream.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-4/README.md)
  * [Item46 优先选择Stream中无副作用的函数](<7 Lambda 和 Stream/Item46 优先选择Stream中无副作用的函数.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-5/README.md)
  * [Item47 作为返回类型，Collection优先于Stream](<7 Lambda 和 Stream/Item47 作为返回类型，Collection优先于Stream.md>)
* [7 Lambda 和 Stream](7-lambda-he-stream-6/README.md)
  * [Item48 谨慎使用stream并行](<7 Lambda 和 Stream/Item48 谨慎使用stream并行.md>)
* [8 方法](8-fang-fa/README.md)
  * [8 方法](<8 方法 /Item49 检查参数的有效性.md>)
* [8 方法](8-fang-fa-1/README.md)
  * [Item50 必要时进行保护性拷贝](<8 方法 /Item50 必要时进行保护性拷贝.md>)
* [8 方法](8-fang-fa-2/README.md)
  * [Item51 谨慎设计方法签名](<8 方法 /Item51 谨慎设计方法签名.md>)
* [8 方法](8-fang-fa-3/README.md)
  * [Item52 谨慎使用重载](<8 方法 /Item52 谨慎使用重载.md>)
* [8 方法](8-fang-fa-4/README.md)
  * [Item53 谨慎使用可变参数](<8 方法 /Item53 谨慎使用可变参数.md>)
* [8 方法](8-fang-fa-5/README.md)
  * [Item54 返回empty的集合或者数组，而不是null](<8 方法 /Item54 返回empty的集合或者数组，而不是null.md>)
* [8 方法](8-fang-fa-6/README.md)
  * [Item55 谨慎地返回Optionals](<8 方法 /Item55 谨慎地返回Optionals.md>)
* [8 方法](8-fang-fa-7/README.md)
  * [Item56 为所有导出的API元素编写文档注释](<8 方法 /Item56 为所有导出的API元素编写文档注释.md>)
* [9 通用编程](9-tong-yong-bian-cheng/README.md)
  * [9 通用编程](<9 通用编程/Item57 局部变量作用域最小化.md>)
* [9 通用编程](9-tong-yong-bian-cheng-1/README.md)
  * [Item58 for-each循环优先于传统的for循环](<9 通用编程/Item58 for-each循环优先于传统的for循环.md>)
* [9 通用编程](9-tong-yong-bian-cheng-2/README.md)
  * [Item59 了解和使用类库](<9 通用编程/Item59 了解和使用类库.md>)
* [9 通用编程](9-tong-yong-bian-cheng-3/README.md)
  * [Item60 如果需要精确的答案，请避免使用float和double](<9 通用编程/Item60 如果需要精确的答案，请避免使用float和double.md>)
* [9 通用编程](9-tong-yong-bian-cheng-4/README.md)
  * [Item61 基本类型优先于封装基本类型](<9 通用编程/Item61 基本类型优先于封装基本类型.md>)
* [9 通用编程](9-tong-yong-bian-cheng-5/README.md)
  * [Item62 当其他类型合适的时候，避免使用字符串](<9 通用编程/Item62 当其他类型合适的时候，避免使用字符串.md>)
* [9 通用编程](9-tong-yong-bian-cheng-6/README.md)
  * [Item63 了解字符串连接的性能](<9 通用编程/Item63 了解字符串连接的性能.md>)
* [9 通用编程](9-tong-yong-bian-cheng-7/README.md)
  * [Item64 使用接口来引用对象](<9 通用编程/Item64 使用接口来引用对象.md>)
* [9 通用编程](9-tong-yong-bian-cheng-8/README.md)
  * [Item65 接口优先于反射](<9 通用编程/Item65 接口优先于反射.md>)
* [9 通用编程](9-tong-yong-bian-cheng-9/README.md)
  * [Item66 谨慎地使用本地方法](<9 通用编程/Item66 谨慎地使用本地方法.md>)
* [9 通用编程](9-tong-yong-bian-cheng-10/README.md)
  * [Item67 谨慎地优化](<9 通用编程/Item67 谨慎地优化.md>)
* [9 通用编程](9-tong-yong-bian-cheng-11/README.md)
  * [Item68 遵守普遍接受的命名规范](<9 通用编程/Item68 遵守普遍接受的命名规范.md>)