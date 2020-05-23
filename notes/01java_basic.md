# Java Basic

### Class and Method

### Class
Class is the basic unit of Java program

- by convention, Class name should be a noun, starts with a uppercase letter
- Class contains methods

### Method
Method contains actions

- by convention, Method name should be a verb, starts with a lowercase letter

```java
public class Person {
    public static void main(String[] args) {
        System.out.println("Hello, world");
    }
}
```

### Entrance of Java Program
The entrance of a Java Program must be:

`public static void main(String[] args){...}`

in a `public` class

## Comments in Java

```java
// single line

/*
comment line 1
comment line 2
...
*/

/**
  * This is a special type of comment
  * This should be written in front of the definition of class or method
  * Then, this will be used to create documentation automatically
*/

```

## Variable and Data Types

two types of variable
- primitive type
- object type

### Primitive type

| data type | num of bytes | range                                      | range              |
| --------- | ------------ | ------------------------------------------ | ------------------ |
| byte      | 1            | -128 ~ 127                                 | -2^(7) ~ 2^(7)-1   |
| short     | 2            | -32768 ~ 32767                             | -2^(15) ~ 2^(15)-1 |
| int       | 4            | -2147483648 ~ 2147483647                   | -2^(31) ~ 2^(31)-1 |
| long      | 8            | -9223372036854775808 ~ 9223372036854775807 | -2^(63) ~ 2^(63)-1 |
| float     | 4            |                                            |                    |
| double    | 8            |                                            |                    |
| char      | 2            |                                            |                    |
| boolean   | 4            |                                            |                    |


### Integer Primitive Type
types:
- byte
- short
- int
- long

- these are the same:
decimal number `15`
binary number: `0b1111`
hexadecimal number: `0xf`

- we can add underscore _ inside number:`int num = 1_000_000;`
- we need to add 'L' at the end of long number, `long l = 900L;`

### Float Primitive Type
types:
- float
- double (Java default float type)

we need to add 'f' at the end of float number:`float f1 = 3.14f;`
`double d1 = 5.5e-5;`

### Boolean

```java
boolean b1 = true;
boolean b2 = false;
```

### Char

- char can represent any Unicode charactor in addition to ASCII
- must use single quote ' instead of "
```java
char a = 'A';
char zhong = '中';
```

### Constant

- adding `final` to variable when declartion makes a constant
- value of constant cannot be changed after initialization
- by convention, constant use all capital letters
```java
final double PI = 3.14;
```

### Var 

- when declare a variable, we can use `var` as a shorthand for long data type
- complier will guess the type from the value assignment

```java
StringBuilder sb = new StringBuilder();

// shorthand
var sb = new StringBuilder();
```

### Variable Scope
the scope of a variable starts from the declartion, ends at the close curly brace

```java

{
    int v = 123; // v scope starts
    {
        int a = 123; // a scope starts
    } // a scope ends
} // v scope ends

```