# Bash Exercise 3

## Have you learned?

- `nano`
- `cat`
- `more`
- `less`

## Instructions

Now your folder structure looks like this:

```
python/
  |__spark/
      |__ README.md
      |__ LICENSE
      |__ INSTALLATION.md
      |__ requirements.txt
      |__ src/
          |__ spark/
                |__ away.py
                |__ tree.py
          |__ main.py
```

Let's add something to `away.py` (P.S. use the CLI).

```
class Away:
    def __init__(self, rows):
        print("*" * rows, end="\n")
        i = (rows // 2) - 1
        j = 2
        while i != 0:
            while j <= (rows - 2):
                print("*" * i, end="")
                print("_" * j, end="")
                print("*" * i, end="\n")
                i = i - 1
                j = j + 2
        print("\n")
```

Now this to `tree.py`.

```
class Tree:
    def __init__(self, n):
        k = n - 1
        for i in range(0, n):
            for j in range(0, k):
                print(end=" ")
            k = k - 1
            for j in range(0, i+1):
                print("* ", end="")
            print("\r")
        print("\n")
```

Now add these last few lines to `main.py`.

```
from spark.away import Away
from spark.tree import Tree

Away(20)
Tree(20)
```

Try running `main.py` if you have Python installed. It should look something like below.

```
********************
*********__*********
********____********
*******______*******
******________******
*****__________*****
****____________****
***______________***
**________________**
*__________________*


         *
        * *
       * * *
      * * * *
     * * * * *
    * * * * * *
   * * * * * * *
  * * * * * * * *
 * * * * * * * * *
* * * * * * * * * *
```

If your output checks, see if you can insert the text from your `LICENSE` file to your `main.py` (use the CLI!).

Run `main.py` again if it works.
