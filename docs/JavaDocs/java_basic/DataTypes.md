# Java 数据类型

在 Java 中，数据类型分为基本数据类型和引用数据类型。下面为你详细介绍。

## 基本数据类型
### 整数类型
| 类型    | 大小（字节） | 范围                  | 示例              |
|---------|--------------|-----------------------|-------------------|
| byte    | 1            | -128 到 127           | `byte b = 100;`    |
| short   | 2            | -32,768 到 32,767     | `short s = 30000;` |
| int     | 4            | -2,147,483,648 到 2,147,483,647 | `int i = 1000000;` |
| long    | 8            | -9,223,372,036,854,775,808 到 9,223,372,036,854,775,807 | `long l = 10000000000L;` |

### 浮点类型
| 类型    | 大小（字节） | 示例              |
|---------|--------------|-------------------|
| float   | 4            | `float f = 3.14f;` |
| double  | 8            | `double d = 3.14;` |

### 字符类型
| 类型    | 大小（字节） | 示例              |
|---------|--------------|-------------------|
| char    | 2            | `char c = 'A';`    |

### 布尔类型
| 类型    | 大小（字节） | 示例              |
|---------|--------------|-------------------|
| boolean | 1            | `boolean flag = true;` |

### 代码示例
```java
public class DataTypesExample {
    public static void main(String[] args) {
        // 整数类型
        byte b = 100;
        short s = 30000;
        int i = 1000000;
        long l = 10000000000L;

        // 浮点类型
        float f = 3.14f;
        double d = 3.14;

        // 字符类型
        char c = 'A';

        // 布尔类型
        boolean flag = true;

        // 输出变量值
        System.out.println("byte: " + b);
        System.out.println("short: " + s);
        System.out.println("int: " + i);
        System.out.println("long: " + l);
        System.out.println("float: " + f);
        System.out.println("double: " + d);
        System.out.println("char: " + c);
        System.out.println("boolean: " + flag);
    }
}
```

## 引用数据类型
引用数据类型包括类、接口、数组等。例如：
```java
// 类
String str = "Hello, Java!";

// 数组
int[] numbers = {1, 2, 3, 4, 5};
```

引用数据类型的变量存储的是对象的引用，而不是对象本身。