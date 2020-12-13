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
