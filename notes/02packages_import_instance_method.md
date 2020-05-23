# Packages, import statments, instance members, default constructor

## import 
- after importing, we can declare a class name using just the class name
- we can also declare it using the full name with package name
- if we do not import package, we must use the full name
- if there exist two classes with the same name, we have to use the full time with package

```java
import com.zhongkailiu.Name; // import class Name from 

public class Person {
    private Name personName;
    // we can also declare with full name like:
    private com.zhongkailiu.Name personName2;
}
```

## this

```java
access to the field of the current object
```

## Comments

```java
// single line comment

/* 
 comment 1
 comment 2
*/
```

## constructor
- Java will add an empty constructor with no parameters by default
- As long as you define a custom constructor in a class, the default empty constructor is gone
