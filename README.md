<h1 align="center"> Python is Kewl! 😎 </h1>
<p align="center"> Exploring Kewl stuff with Python 🐍 </p>

Python can do a lot of wonderful stuff, Here is just a repo , showing all the cool stuff you can do with Python. 


(I'll be adding stuff as i see)


So, Here we go,

**Note:** All the examples are tested on Python 3.5.2 interactive interpreter, and they should work for all the Python versions unless explicitly specified before the output.

# Table of Contents 

<!-- Generated using "markdown-toc -i README.md --maxdepth 3"-->
<!-- toc -->

- [▶ Self Replicating Python Code(Quines)](#quines)
- [▶ Quine generator (Introns)](#introns)

<!-- tocstop -->

> ### ▶ Quines
> ```py
> s='s=%r;print(s%%s)';print(s%s)
> ```
#### 💡 Explanation:

So, this python code is a quine, i.e. The output is the program itself. It can be called a quine if it's not an empty program , and is self sustained.
(No file reading/writing operations). Imagine our DNA coded like this and it self replicates , [Try it online!](https://tio.run/##K6gsycjPM/7/v9hWvdhWtci6oCgzr0SjWFW1WFMdzinW/P8fAA "Python 3 – Try It Online")

The code has two parts , Data and the output.
> DATA part
> ```py
> s='s=%r;print(s%%s)'
> ```
>
> OUTPUT producing part
> ```py
> print(s%s)
> ```

The Variable s is assigned the above string. the %r provides a repr() version of the string that's passed as a format specifier. Basically if %s was used, it doesn't display the quotation marks, but %r does. %%s is used to escape the %s and to indicate that %s is not a format specifier. Then we print the string s and pass s to %r which equates to repr(s). thus printing the whole code. This shows the beauty of code replication. Imagine if some code like this was present in DNA and it uses this to replicate. 


> ### ▶ Introns
> ```py
> t='';s='t=input()or t;print(f"t={repr(t)};s={repr(s)};exec(s)#{t}")';exec(s)#
> ```

#### 💡 Explanation:

So, this python code is an Intron, i.e. it is a quine in itself but can GROW by mutation of some kind. Weirded out? I was too...

Check this out. The code in itself is a quine, i.e. if you provide an empty input to it, (a newline) it'll output the program itself. But, if you provide some input, It'll will produce a modified intron that has the string in it (Yes, it still remains a quine and you can run the output again!)

> INPUT 
> ```py
> BINOD
> ```
> OUTPUT
> ```py
> t='BINOD';s='t=input()or t;print(f"t={repr(t)};s={repr(s)};exec(s)#{t}")';exec(s)#BINOD
> ```

Kewl, isn't it? Now you can take the Output and run it again!
> CODE
> ```py
> t='BINOD';s='t=input()or t;print(f"t={repr(t)};s={repr(s)};exec(s)#{t}")';exec(s)#BINOD
> ```
>
> INPUT
> ```py
> Demoknight tf2
> ```
>
> OUTPUT
> ```py
> t='Demoknight tf2';s='t=input()or t;print(f"t={repr(t)};s={repr(s)};exec(s)#{t}")';exec(s)#Demoknight tf2
> ```

The code mutated again!

What if, you supplied the original intron into the intron itself?? Why don't you [Try it Yourself?](https://tio.run/##K6gsycjPM/7/v8RWXd262Fa9xDYzr6C0REMzv0ihxLqgKDOvRCNNqcS2uii1oEijRLMWqAjCLgayUytSk4EM5eqSWiVNdTj3/38uAA "Python 3 – Try It Online")

