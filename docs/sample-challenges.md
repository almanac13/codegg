## Challenge 1: Two increments

- **Topic:** Java operators
- **Difficulty:** Easy
- **Format:** Predict the output

### Code snippet

```java
int x = 5;
System.out.println(x++ + ++x);
```

### Question

What does this code print?

### Answer options

A. 10
B. 11
C. 12
D. 13

### Correct option

C. 12

### Explanation

Java evaluates the operands from left to right.

1. Initially, x is 5.
2. x++ produces the current value, 5, then increases x to 6.
3. ++x increases x from 6 to 7, then produces 7.
4. The expression adds 5 + 7, so the output is 12.

After the expression, x is 7.

### Hint

Track x after each increment. Post-increment and pre-increment
produce their values at different moments.
## Challenge 2: One step too far

- **Topic:** Arrays and loops
- **Difficulty:** Easy
- **Format:** Find the error

### Code snippet

```java
int[] numbers = {10, 20, 30};

for (int i = 0; i <= numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

### Question

Why does this code throw an ArrayIndexOutOfBoundsException?

### Answer options

A. Array indices must start at 1.
B. The loop allows i to reach an invalid array index.
C. The array contains too few values to use a loop.
D. System.out.println cannot print array elements.

### Correct option

B.

### Explanation

The array has three elements, with valid indices 0, 1, and 2.

numbers.length is 3. The condition i <= numbers.length allows
the loop to run when i is 3.

Accessing numbers[3] throws ArrayIndexOutOfBoundsException.

The program prints 10, 20, and 30 before the exception occurs.

### Hint

Compare the array's length with its last valid index.

## Challenge 3: Where did the decimal go?

- **Topic:** Integer division and type conversion
- **Difficulty:** Easy
- **Format:** Choose the fix

### Code snippet

```java
int total = 7;
int count = 2;

double average = total / count;

System.out.println(average);
```

### Question

The expected average is 3.5, but the program prints 3.0.
Which replacement correctly calculates the average?

### Answer options

A. double average = (double) (total / count);
B. double average = (double) total / count;
C. double average = total / count * 1.0;
D. double average = Math.round(total / count);

### Correct option

B.

### Explanation

Both operands are integers, so total / count uses integer
division. It produces 3, discarding the fractional part.
Assigning 3 to a double then produces 3.0.

Casting total before division changes the calculation to
floating-point division:

(double) total / count
7.0 / 2
3.5

Options A and C convert the result after integer division
has already discarded the fractional part.

Option D rounds a value that is already 3.

### Hint

Convert an operand before dividing, rather than converting
the result afterward.
