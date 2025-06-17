# Java 控制流程

在 Java 中，控制流程语句用于控制程序的执行顺序。下面介绍几种常见的控制流程语句。

## 条件语句
### if - else 语句
`if - else` 语句根据条件判断执行不同的代码块。
```java
public class IfElseExample {
    public static void main(String[] args) {
        int num = 10;
        if (num > 0) {
            System.out.println("数字是正数");
        } else if (num < 0) {
            System.out.println("数字是负数");
        } else {
            System.out.println("数字是零");
        }
    }
}
```

### switch 语句
`switch` 语句根据表达式的值执行不同的分支。
```java
public class SwitchExample {
    public static void main(String[] args) {
        int day = 3;
        switch (day) {
            case 1:
                System.out.println("星期一");
                break;
            case 2:
                System.out.println("星期二");
                break;
            case 3:
                System.out.println("星期三");
                break;
            default:
                System.out.println("其他");
        }
    }
}
```

## 循环语句
### for 循环
`for` 循环用于已知循环次数的情况。
```java
public class ForLoopExample {
    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            System.out.println("当前数字: " + i);
        }
    }
}
```

### while 循环
`while` 循环在条件为真时重复执行代码块。
```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 0;
        while (i < 5) {
            System.out.println("当前数字: " + i);
            i++;
        }
    }
}
```

### do - while 循环
`do - while` 循环至少执行一次代码块，然后再判断条件。
```java
public class DoWhileLoopExample {
    public static void main(String[] args) {
        int i = 0;
        do {
            System.out.println("当前数字: " + i);
            i++;
        } while (i < 5);
    }
}
```

## 跳转语句
### break 语句
`break` 语句用于终止当前循环或 `switch` 语句。
```java
public class BreakExample {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5) {
                break;
            }
            System.out.println("当前数字: " + i);
        }
    }
}
```

### continue 语句
`continue` 语句用于跳过当前循环的剩余部分，继续下一次循环。
```java
public class ContinueExample {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5) {
                continue;
            }
            System.out.println("当前数字: " + i);
        }
    }
}