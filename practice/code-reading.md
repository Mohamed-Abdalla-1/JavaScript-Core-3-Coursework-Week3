# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
The firs log has the value of x that been declared within the function scope, the second log has a global scope.
## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
Undefined, because x value hasn't been passed to the function or declared inside it.
Undefined, because y value only declared within the function scope.
## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.

f1(x): return 10

console.log(x): it will console log 9, it gits the value of x from the global scope not from the function

f2(y): return 10

console.log(y):it will console log { x: 9 } , it gits the value of y from the global scope not from the function