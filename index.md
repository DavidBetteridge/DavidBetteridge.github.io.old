
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
private int Largest(int value1, int value2) => (value1 - value2) > 0 ? value1 : value2;
```



# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/DavidBetteridge/DavidBetteridge.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
