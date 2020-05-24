# keywords

## package

- package name is like a folder name of codes
- avoid file name clashes
- domain name can be a good package name
- must declare package name at the first line in java program

```java
package com.zhongkailiu.learnjava
```

## import 
- use others' codes
- can import one file or all files

```java
import com.zhongkailiu.learnjava.*
```

## class

- by convention, class name should be a noun, starting with a capital letter
- keep class size small, to improve reuseability and readability

```java
class Car {

}
```

## method

- by convention, method name should be a verb to describe the actions
- recommend 3 - 20 lines of codes in a method
- recommend 0 - 5 parameters in a method
- **structure and readability is important**
- types: 
  - query method
    - return something, but does not change values
  - command method
    - does not return, but change values

```java
drive(spped) {
    
}
```

## variable

- value of a variable can change in the running of the program

## public

- access modifier 
- any class in any package can access public class or method

## void

- every method must define a return type
- method with no return, return `void`


```java
public class Car {
    public void drive(speed) {
        ...
    }
}
```

## @Test

- @ symbol indicates an anotation
- @Test indicates a class will be used to test

## Camel Case
- variable names by convention are camel case

```java
myNewCar = new Car();
```


## dot . 

- call a method on a class

```java
car.drive(100)
```

## colon ; 

- indicate the end of a code line

```java
@Test
public void shouldDrive() {
    car.drive(100);
}
```

## object
- class is a template of object

## object oriented language
- Java is OOP

## constructor
- create a new object of a certain type of class

```java
new Car(10, 120);
```

## variable declaration
- declare the type of a variable

```java
Car myCar;
```

## object allocation

```java
Car myCar = new Car(10, 120);
```

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
