## A testing test

I was reading an article on testing the other night and it claimed that 100% code coverage is not really enough.  As I agreed with the most things which were said I thought that I would come up with a fun example to demostrate this.

### The test

Given the following (c#) function which returns the largest of 2 numbers,  what tests would you write?


```markdown
 private int Largest(int value1, int value2)
```

**HAVE A THINK BEFORE READING ON!**




I expect you came up with tests along the following lines:

- The first number is largest   
- The second number is largest
- Both numbers are equal

```markdown
Assert.AreEqual (4,  Largest(3,4));
Assert.AreEqual (5,  Largest(5,4));
Assert.AreEqual (6,  Largest(6,6));
```

and if you thought I was trying to trick you then you might also include a couple of edge cases such as 


```markdown
Assert.AreEqual (0,  Largest(0,0));
Assert.AreEqual (1,  Largest(1,0));
```


### The source code
I'm now going to let you see the body of the function.  Clearly we already have 100% test coverage,  but would you write an additional tests?

```markdown
private int Largest(int value1, int value2) 
              => (value1 - value2) > 0 ? value1 : value2;
```

**HAVE A THINK BEFORE READING ON!**

As there is some subtraction going on,  prehaps we ought to include some tests for negative numbers.

```markdown
Assert.AreEqual (0,  Largest(0,-10));
Assert.AreEqual (-10,  Largest(-10,-20));
```

So we are now update to 7 unit tests for our one line of code,  but we haven't yet found the bug.


