
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/588ec7e9-377c-4f01-a92f-2d4e5796a441" />
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/64a36996-0d63-4382-a0a4-4740def1289d" />
<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/6670307e-026d-4b64-a291-d930d9a516f8" />






# Bash Calculator

A simple command-line calculator built using **Bash Shell Scripting**.
The program accepts two numbers from the user and performs addition,
subtraction, multiplication, or division based on the selected
operation.

## 📌 Project Overview

This project demonstrates the basic concepts of Bash scripting,
including:

-   Taking user input with `read`
-   Displaying output using `echo`
-   Arithmetic operations
-   `case` statements for menu-based selection
-   `if-else` conditional statements
-   Division-by-zero validation
-   Executing a Bash script using `./filename.sh`

## ✨ Features

-   Addition of two numbers
-   Subtraction of two numbers
-   Multiplication of two numbers
-   Division of two numbers
-   Prevents division by zero
-   Handles invalid operation choices
-   Simple and beginner-friendly command-line interface

## 🛠️ Technologies Used

  Technology            Purpose
  --------------------- -----------------------------------
  Bash                  Shell scripting and program logic
  Linux/Unix Terminal   Running the script
  GNU Nano              Creating/editing the script

## 📂 Project Structure

``` text
calculator/
└── calculator.sh
```

## 🚀 How to Run

### 1. Create the Bash file

Create a file named:

``` bash
calculator.sh
```

### 2. Add the script

``` bash
#!/bin/bash

echo "======================"
echo "      calculator"
echo "======================"

echo "enter first number:"
read a

echo "enter second number:"
read b

echo "choose operation:"
echo "1. addition (+)"
echo "2. subtraction (-)"
echo "3. multiplication (*)"
echo "4. division (/)"

read choice

case $choice in
1)
    echo "result = $((a + b))"
    ;;

2)
    echo "result = $((a - b))"
    ;;

3)
    echo "result = $((a * b))"
    ;;

4)
    if [ $b -eq 0 ]; then
        echo "cannot divide by zero"
    else
        echo "result = $((a / b))"
    fi
    ;;

*)
    echo "INVALID CHOICE"
    ;;

esac
```

### 3. Give execute permission

Open the terminal in the project directory and run:

``` bash
chmod +x calculator.sh
```

### 4. Run the calculator

``` bash
./calculator.sh
```

## 💻 Example

### Input

``` text
======================
      calculator
======================
enter first number:
7
enter second number:
7
choose operation:
1. addition (+)
2. subtraction (-)
3. multiplication (*)
4. division (/)
1
```

### Output

``` text
result = 14
```

## 🔢 Available Operations

  Choice   Operation        Example     Result
  -------- ---------------- --------- --------
  1        Addition         7 + 7           14
  2        Subtraction      10 - 4           6
  3        Multiplication   5 \* 3          15
  4        Division         20 / 5           4

> **Note:** Bash arithmetic using `$((...))` performs integer
> arithmetic. For example, `5 / 2` produces `2`.

## 🛡️ Error Handling

### Division by Zero

The script checks whether the second number is zero before performing
division.

``` bash
if [ $b -eq 0 ]; then
    echo "cannot divide by zero"
```

If the user enters `0` as the second number, the program displays:

``` text
cannot divide by zero
```

### Invalid Choice

If the user enters a number other than `1`, `2`, `3`, or `4`, the
default `*)` case displays:

``` text
INVALID CHOICE
```

## 🧠 Bash Concepts Demonstrated

### 1. Variables

``` bash
read a
read b
```

The values entered by the user are stored in variables `a` and `b`.

### 2. Arithmetic Expansion

``` bash
$((a + b))
```

Bash uses `$((...))` for integer arithmetic.

### 3. Case Statement

``` bash
case $choice in
```

The `case` statement selects the operation according to the user's menu
choice.

### 4. Conditional Statement

``` bash
if [ $b -eq 0 ]; then
```

This checks whether division by zero would occur.

## 📋 Requirements

To run this project, you need:

-   Linux, macOS, WSL, or another Bash-compatible environment
-   Bash shell
-   Terminal

Check your Bash version with:

``` bash
bash --version
```

## 🔮 Future Enhancements

Possible improvements include:

-   Add decimal/floating-point calculations using `bc`
-   Add a loop so multiple calculations can be performed without
    restarting
-   Add a "Exit" option
-   Improve input validation
-   Add percentage and modulus operations
-   Create a more advanced menu interface
-   Store calculation history

## 🎯 Learning Objective

The main objective of this project is to understand the fundamentals of
**Bash shell scripting** by creating a practical command-line
calculator. It is suitable as a beginner Linux/Shell Scripting project.


GitHub.
