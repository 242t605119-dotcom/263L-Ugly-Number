# Ugly Number

**LeetCode Problem:** 263
**Language:** Python

## Problem

An **ugly number** is a positive number whose prime factors are only `2`, `3`, and `5`.

Given an integer `n`, determine whether it is an ugly number.

Return `True` if it is an ugly number. Otherwise, return `False`.

## Example

Input:

```text
n = 6
```

The number can be divided by `2` and `3`:

```text
6 → 3 → 1
```

So its prime factors are only `2` and `3`.

Output:

```text
True
```

Another example:

```text
n = 14
```

Since:

```text
14 = 2 × 7
```

It contains the prime factor `7`.

Output:

```text
False
```

## Approach

First, check whether the number is positive.

If `n` is less than or equal to `0`, it cannot be an ugly number.

Then repeatedly divide `n` by:

```text
2
3
5
```

Whenever the number is completely divisible by one of these factors, we divide it.

For example:

```text
n = 60

60 ÷ 2 = 30
30 ÷ 2 = 15
15 ÷ 3 = 5
5 ÷ 5 = 1
```

The final value is `1`, so `60` is an ugly number.

If the final value is not `1`, it means another prime factor exists, so the number is not ugly.

## Key Idea

An ugly number must be completely reduced to `1` by repeatedly removing factors of `2`, `3`, and `5`.

## Complexity

* **Time:** O(log n)
* **Space:** O(1)

Only a few variables are used, so the extra space remains constant.

## Key Learning

This problem helped me practice:

* Prime factors
* Modulo operator
* Integer division
* Loops
* Number manipulation
* Mathematical problem solving

## Conclusion

The solution repeatedly removes the factors `2`, `3`, and `5` from the given number. If the remaining value is `1`, the number is an ugly number.

**Author: T. Nandhini**
