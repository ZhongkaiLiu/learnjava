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
- reference type

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

these are the same:
- decimal number `15`
- binary number: `0b1111`
- hexadecimal number: `0xf`

we can add underscore _ inside number:`int num = 1_000_000;`

we need to add 'L' at the end of long number, `long l = 900L;`

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

## Integer Calculation

### The result of integer division is also integer
```java
int p = 16 / 5; // p == 3
int q = 16 % 5; // p == 6
```

### Overflow
when a number increase beyond the maximum value of the data type, it will change to a wrong value. To solve this, we need to change `int` to `long`

### bitwise operations

- bitwise move left (*2) or move right (/2)
```java
int n = 6; // 0110
int a = n << 1; // move left to 1100 == 12, new bits are 0
int b = n >> 1; // move right to 0011 == 3, does not move sign bit (the hightest bit), new bits are 0
int m = -6; // 1010
int c = m >> 1; // move right to 1101 == -7, does not move the sign bit (the hightest bit), new bits are 1 
int d = m >>> 1; // move right to 0101 == 5, move the sign bit (the hightest bit), new bits are 0
```

- bitwise AND, OR, NOT, XOR
```java
n = 0 & 1; // biwise AND
n = 0 | 1; // bitwise OR
n = ~ 0; // bitwise NOT
n = 0 ^ 1; // bitwise XOR
```

### data type conversion

- smaller type can be automatically convert to larger type

```java 
short s = 123;
int x = s + 12345678;
```

- forced type conversion

```java
int n = 123;
short s = (short) n;
```

## Float Calculation

### Not accurate
when compare two float number, should not use `f1==f2`, instead, we should check whether the difference is small enough `Math.abs(f1-f2) < 0.00001`

## Overflow
when float divided by 0, no error but return special value
```java
double d1 = 0.0 / 0; // NaN (Not a Number)
double d2 = 1.0 / 0; // Infinity
double d3 = -1.0 / 0; // -Infinity
```

## Type Conversion

- convert `double` to `int`
```java
int n1 = (int) 12.7; // 12
```
- when integer calculate with float number, integer convert to float number automatically
```java
int n = 3;
double d = 12.3 + n; // d == 15.3
```

## Boolean Calculation

### compare operations
```java
a > b;
a >= b;
a < b;
a <= b;
a == b;
a != b;
```
### logical operations
```java
a && b; // AND
a || b; // OR
!a; // NOT
```
- logical operations are short-circuited 
- `true || (exp1)` will return `true` directly without calculating `exp1`
- `false && (exp2)` will return `false` directly without calculating `exp2`

### Ternary operator

```java
boolean b;
int z = b ? x : y; // if b is true, return x, otherwise return y
```

## Char and String

### Char 
- char use single quote
- one char store one Unicode character

### String
- string use double quotes
- escape "\"
- String object is immutable

```java
String s1 = "Hello, \"Kevin\"";
```

### null
- any reference variable can be `null`, which means it does NOT reference any object
- `null` value is differenct from empty string `""`
```java
String s1 = null;
String s2 = "";
```
