# Control Flow

## If statement

```java
if (exp1) {
    ...
} else if (exp2) {
    ...
} else {
    ...
}
```

### compare two variables
- for primitive variables, we can use `val1 == val2`
- for reference variables, `ref1 == ref2` check whether they reference the same object (stores the same address)
- for reference variables, we must use `ref1.equals(ref2)` to compare the equality of the values of them

## Switch statement

```java
switch (option) {
    case 1:
        ...;
        break;
    case 2:
        ...;
        break;
    default:
        ...;
        break;
}
```