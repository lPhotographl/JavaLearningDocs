# Java 面向对象编程

面向对象编程（Object-Oriented Programming, OOP）是 Java 的核心编程范式，它将数据和操作数据的方法封装在一起，形成对象。下面介绍面向对象编程的几个重要概念。

## 类和对象
### 类
类是对具有相同属性和行为的对象的抽象描述。以下是一个简单的类定义示例：
```java
// 定义一个 Person 类
class Person {
    // 成员变量
    String name;
    int age;

    // 构造方法
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // 成员方法
    public void introduce() {
        System.out.println("我叫" + name + "，今年" + age + "岁。");
    }
}
```

### 对象
对象是类的实例。通过 `new` 关键字创建对象。
```java
public class ClassAndObjectExample {
    public static void main(String[] args) {
        // 创建 Person 对象
        Person person = new Person("张三", 20);
        // 调用对象的方法
        person.introduce();
    }
}
```

## 封装
封装是将对象的属性和方法封装在一起，通过访问控制符（如 `private`、`public`）来控制对属性的访问。
```java
class Student {
    // 使用 private 修饰属性，实现封装
    private String name;
    private int age;

    // 提供公共的 getter 和 setter 方法
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age > 0 && age < 150) {
            this.age = age;
        }
    }
}
```

## 继承
继承是指一个类可以继承另一个类的属性和方法，从而实现代码的复用。
```java
// 父类
class Animal {
    public void eat() {
        System.out.println("动物吃东西");
    }
}

// 子类，继承自 Animal 类
class Dog extends Animal {
    public void bark() {
        System.out.println("汪汪汪");
    }
}

public class InheritanceExample {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // 调用父类的方法
        dog.bark(); // 调用子类的方法
    }
}
```

## 多态
多态是指同一个方法调用，由于对象不同可能会有不同的行为。
```java
// 父类
abstract class Shape {
    public abstract double area();
}

// 子类：圆形
class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    public double area() {
        return Math.PI * radius * radius;
    }
}

// 子类：矩形
class Rectangle extends Shape {
    private double width;
    private double height;

    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    @Override
    public double area() {
        return width * height;
    }
}

public class PolymorphismExample {
    public static void main(String[] args) {
        Shape circle = new Circle(5);
        Shape rectangle = new Rectangle(4, 6);

        System.out.println("圆形面积: " + circle.area());
        System.out.println("矩形面积: " + rectangle.area());
    }
}