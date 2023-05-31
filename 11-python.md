# Python <!-- omit in toc -->

I already did the [Automate The Boring Stuff](https://github.com/dallas-hall/learning-python) and [Python Crash Course](https://github.com/dallas-hall/learning-python) textbooks. So the only thing documented here is new or something I didn't know.

## Table of Contents <!-- omit in toc -->

- [1) Certification](#1-certification)
- [2) Literals](#2-literals)
- [3) Operators](#3-operators)
- [4) Strings](#4-strings)
- [5) Bitwise Operators](#5-bitwise-operators)
  - [5.1) Conjunction (AND) Example](#51-conjunction-and-example)
  - [5.2) Disjunction (OR)Example](#52-disjunction-orexample)
  - [5.3) Exclusive Or (XOR) Example](#53-exclusive-or-xor-example)
  - [5.4) Negation (NOT) Example](#54-negation-not-example)
  - [5.5) Bitwise Operation Shortcuts](#55-bitwise-operation-shortcuts)
- [6) Bit Shifting](#6-bit-shifting)
  - [6.1) Bit Shifting Right Example](#61-bit-shifting-right-example)
  - [6.2) Bit Shifting Left Example](#62-bit-shifting-left-example)
  - [6.3) Division \& Multiplication](#63-division--multiplication)

## 1) Certification

The [OpenEDG Python Institute](https://pythoninstitute.org/) offers [Python programming certification.](https://pythoninstitute.org/certification-tracks)

## 2) Literals

* You can add `_` to numbers to make them more readable. e.g. `1_000_000`.
* Octal numbers start with `0o`, e.g. `0o123`
* Scientific numbers can be written as number, e, followed by plus or minus, and the amount to shift the decimal. e.g. `1e+2 = 100` and `1e-2 = 0.01`

## 3) Operators

![](./images/python08.png)

## 4) Strings

Multiplying a string by 0 or negative number returns an empty string.

## 5) Bitwise Operators

Bitwise operators are characters that represent actions (bitwise operations) to be performed on single bits. In Python there are:
* `&` conjunction (AND), 1 and 1 is 1. Everything else is 0.
* `|` disjunction (OR), two 0s is 0. Everything else is 1.
* `^` exclusive (XOR), 0 and 1 or 1 and 0 is 1. Everything else is 0.
* `~` negation (NOT), returns 1 for every 0 and 0 for every 1.

![](./images/python09.png)

### 5.1) Conjunction (AND) Example

Here is an example of `15 & 22 = 6`

![](./images/python10.png)

![](./images/python11.png)

### 5.2) Disjunction (OR)Example

Here is an example of `15 | 22 = 31`

![](./images/python12.png)

### 5.3) Exclusive Or (XOR) Example

Here is an example of `15 ^ 22 = 25`

![](./images/python13.png)

### 5.4) Negation (NOT) Example

Here is an example of `~22 = -23`

![](./images/python14.png)

### 5.5) Bitwise Operation Shortcuts

Like arithmetic, there are bitwise operation shortcuts.

![](./images/python15.png)

## 6) Bit Shifting

The bit shifting operators do exactly what their name implies. They shift bits.
* `>>` move all the bits to the right by *n*.
* `<<` move all the bits to the left by *n*.

![](./images/python16.png)

### 6.1) Bit Shifting Right Example

Here is an example of `22 >> 1 = 11`. We are shifting the bits to the right by 1 place. Bit shifting right by 1 is dividing by 2.

![](./images/python17.png)

### 6.2) Bit Shifting Left Example

Here is an example of `22 << 1 = 44`. We are shifting the bits to the right by 1 place. Bit shifting left by 1 is mutliplying by 2.

![](./images/python18.png)

### 6.3) Division & Multiplication

You can use the left shift for division and the right shit for multiplication. e.g.
* Bit shifting right by 1 is dividing by 2.
* Bit shifting right by 2 is dividing by 4. etc.
* Bit shifting left by 1 is mutliplying by 2.
* Bit shifting left by 2 is mutliplying by 4. etc

![](./images/python19.png)
