<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/c-programming.png"> 
  <h1>C Questions</h1>

<span>Here I've just posted multiple **C programming language** question to share the capability of language and also allow people to test their knowledge in this language.

It can be used as a tool to prepare yourself for interviews or opening new thoughts on the language itself.

The answer and its short description, is available in the **collapsed sections** below the questions.
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
- C: `9 8 7 6 5 4 3 2 1 0`
- D: It will print `10` indefinitely

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

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

###### 3. Assume we have a function called foo as follows:

```c
int foo(int f(int,int), int x) {
    ...
}
```

Is the first parameter valid? If it is valid, what is it? And if it’s not valid, what kind of error it will produce?

- A: Yes, it is valid and it is a function pointer
- B: No, it is not a valid parameter and it will lead to a syntax error
- C: No, it is not a valid parameter and it will lead to a semantic error
- D: Yes, it is valid and it is a C language built-in function

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

It is an ordinary function pointer and it will interpret as `int (*f)(int,int)`.

</p>
</details>

---

###### 4. What's the output?

```c
void foo() {
   static int i = 5;

   printf("%d ", ++i);
}

void main() {
    int i;

    for (i = 0; i < 3; ++i)
        foo();
}
```

- A: `1 2 3`
- B: `6 6 6`
- C: `6 7 8`
- D: `5 6 7`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

When we define a variable with `static` it will act like a closure so it will remember the last value of itself each time we running it, it will increment the previous value instead of resetting the value to `5`.

Also, we have to keep in mind the `++i` _(prefix)_ will first increment the value and then assign/return it. So the first call of `foo()` will print `6` for us.

</p>
</details>

---

###### 5. What's the output?

```c
int i = 0;

for(i = 0; i < 3; i++) {
   if (i = 2)
      continue;
   printf("%d ", i);
}
```

- A: `0 1 2`
- B: `0 1`
- C: `0 1 2 3`
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

There is a difference between comparison and assigning. In this case we are assigning the value of `2` to `i` _(i=2)_, whilst we have to compare them with double equal signs. So, since we've used `continue` the print command will be escaped here.

</p>
</details>

---

###### 6. What's the output?

```c
int i = 1;

while (i < 10)
   printf ("%d\n", i);
```

- A: It will print 1 indefinitely
- B: `1`
- C: `10`
- D: `1 2 3 4 5 6 7 8 9`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

We don not increment the `i` at any moment, so the condition will always be true and the value of `i` will be always equal to `1`.

</p>
</details>

---

###### 7. what is/are the difference(s) between `malloc()` and `calloc()` memory allocation?

- A: There is no major difference and they both allocate memory from heap area/dynamic memory
- B: `malloc()` initializes the allocated memory block to zero whilst `calloc()` does not initialize it
- C: `calloc()` initializes the allocated memory block to zero whilst `malloc()` does not initialize it
- D: `calloc()` will take two arguments whilst `malloc()` will only take one

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C and D

`calloc()` and `malloc()` both are responsible for allocating memory. `calloc()` will initialize the allocated memory block to zero, whilst `malloc()` doesn’t initialize it. If we try to access the content of the memory block(before initializing) then we’ll get a segmentation fault error(or maybe garbage values), but if we try to do the same thing with `calloc()` we will get `0`. Also, `calloc ()` will take two arguments, the first one is a number of blocks to be allocated and the second one is the size of each block, whilst `malloc ()` will only get one argument and it is for the size of each block.

</p>
</details>

---

###### 8. What is a dangling pointer?

- A: A pointer which points to a deleted memory address
- B: A pointer which points to a static variable
- C: A pointer which points to a freed memory address
- D: A pointer which points to some data without any specific type

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A and C

A dangling pointer is a pointer that points to invalid data or to data which is not valid anymore. So, it can pointers to deleted and freed memory addresses will be counted as dangling pointers.

</p>
</details>

---

###### 9. What is a wild pointer?

- A: A pointer which has not been initialized to anything
- B: A pointer which points to a garbage memory location
- C: A pointer which is initialized to NULL
- D: A pointer which points to a freed memory address

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A and B

A pointer which has not been initialized to anything (not even NULL) is known as a wild pointer. Also, the pointer may be initialized to a non-NULL garbage value that may not be a valid address. So, if any pointer points to uninitialized or garbage location we call it wild pointer.

</p>
</details>

---

###### 10. What's the output?

```c
printf("\");
```

- A: `\`
- B: `''`
- C: It will produce a syntax error
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

`\` is an escape sign, but in this particular situation there is nothing to be escaped in the `printf` so, it will escape the `"` _(double quote sign)_ and it will lead to syntax errors, because, there will be no closing quotes in the `printf` anymore.

</p>
</details>

---

###### 11. What's the output?

```c
printf("'\'");
```

- A: `\`
- B: `''`
- C: It will produce a syntax error
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`\` is an escape sign, in this particular case it will escape the second `'` _(quote sign)_, so, it won't change anything here and the printed element will be `''`.

</p>
</details>

---

###### 12. What's the output?

```c
printf("\\");
```

- A: `\`
- B: `''`
- C: It will produce a syntax error
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`\` is an escape sign, in this particular case it will escape the second `\`, so, the final output will be `\`.

</p>
</details>

---

###### 13. What's the output?

```c
short int i;

for (i = 32765; i < 32768; i++)
    printf ("%d\n", i);
```

- A: `32765 32766 32767`
- B: `32766 32767 32768`
- C: It will run indefinitely
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The max value for `short` variables are `32767`, so, the condition _(`i < 32768`)_ will be never met.

</p>
</details>

---

###### 14. What's the output?

```c
float i = 30;

while (f != 31.0) {
    printf ("%f\n", f);
    f += 0.1;
}
```

- A: `30.1 30.2 30.3 30.4 30.5 30.6 30.7 30.8 30.9`
- B: `30.000000 30.100000 30.200001 30.300001 30.400002 30.500002 30.600002 30.700003 30.800003 30.900003`
- C: It will run indefinitely
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The floating point variables will automatically cast to float variables, whether the initialization is int or whatever else. So, `30` will cast to `30.000000`. Because of this, in this particular case, the condition will be never met _(`f != 31.0`)_ so, the code will add up `0.1` to the initial value until memory gets overflow.

</p>
</details>

---

###### 15. What's the output?

```c
int i = 0;

while(i<=5);
printf("%d\n", i);
```

- A: `0 1 2 3 4 5`
- B: `0 1 2 3 4`
- C: `0.0 1.0 2.0 3.0 4.0 5.0`
- D: It won't print anything

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

If you take a closer look at the snippet you will notice _(`while(i<=5);`)_ a semicolon _(`;`)_ after the `while` statement, so, it will produce a null statement inside the `while` loop _(`while(i<=5){ ; }`)_ and the snippet will be executing indefinitely because of that and never reaches the `printf` expression.

</p>
</details>

---
