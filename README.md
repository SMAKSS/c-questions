<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/c-programming.png"> 
  <h1>C Questions</h1>

<span>Here I've just posted multiple **C programming language** question to share the capability of language and also allow people to test their knowledge in this language. 

It can be used as a tool to prepare yourself for interviews or opening new thoughts on the language itself.

The answer and the short description of it, is available in the **collapsed sections** below the questions.
</span>
</div>

---
###### 1. What's the output?

```c
int x = 10;

while (x --> 0)
  printf("%d ", x);
```

- A: It will produce a syntax error
- B: `0`
- C: It will print `10` indefinitely
- D: `9 8 7 6 5 4 3 2 1 0`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

This is a simple loop over variable `x`. In the loop condition, we just decrementing `x` in each iteration (`x--` or `x --` equals to `x = x - 1`) until it gets equal to `0`.

</p>
</details>

---

###### 2. What's the output?

```c
int x = 10;

while (x --\
            \
             \
              \
               > 0)
     printf("%d ", x);
```

- A: It will produce a syntax error
- B: `∞`
- C: `0`
- D: `9 8 7 6 5 4 3 2 1 0`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

This is the same question as the [question 1](#1.-What's-the-output?).

This is a simple loop over variable `x`. In the loop condition, we just decrementing `x` in each iteration (`x--` or `x --` equals to `x = x - 1`) until it gets equal to `0`.

The only difference between these two questions is about ignoring the `\` by the compiler whilst there is a next line (`\n`) appears after it.

</p>
</details>

---