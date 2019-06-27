# Sample exercise

Recursion functions sometimes uses a lot of space (stack frames), because they need to store all the intermediate states of the calculation. This is not considered as such a good practice as it can slow down the computer quite a lot. That is why we introduced tail-recursion, which call itself as its last action and the function's stack frame can be reused.

* In this exercise you will design a tail recursion version of given factorial function:

```scala
def factorial(n: Int): Int =
	if (n == 0) 1 else n * factorial(n-1)
```

* Fill in the "if-else" conditional, where you call the function "loop" with appropriate parameters in a tail recursion way

* Fill in the first parameter in a function call "loop"

## Tail recursion version:

```scala
def factorial(n: Int): Int = {
	def loop(acc: Int, n: Int): Int =
		// Add your if-else conditional here

	loop(???, n) 
}
```


## Solution:

### if-else conditional:

```scala
if (n == 0) acc
else loop(acc * n, n-1)
```

### Question marks need to be replaced with 1
```scala
loop(1, n)
```
