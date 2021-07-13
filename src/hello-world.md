# Hello, World
Now that f(x) is up and running, it's time to write our very first program in fxlang. It's a tradtion to start a new language with printing `Hello, World!` to the standard output. 
> Note: fxlang is still in dev stage. Much of it consists of basic grammar from `Crafting Interpreters` and is just a toy interpreter for now. I'll try to give some more time to it to rewrite in a better "rusty" manner. Also, there is no Language Server Protocol(LSP) yet so features like autocomplete and syntax highlighting is not on the roadmap yet.

## Creating a Script File
We'll start off by making a `.fx` file to write the fx code. fxlang files always end with `.fx`. Choose a directory of your own choice. Here I'll show an creating an example file and writing the code in it.

Open a terminal and enter the following commands to make a `.fx` file.

```console
$ touch helloWorld.fx
$ vim helloWorld.fx
```

I use Vim editor, you can use any editor you like(VSCode, Atom etc). 

> Notice, we use lowerCamelCase as the standard to write fx code.

## Writing and Running fx Program
Now, in the editor we will write the following code. 

<span class="filename">Filename: main.rs</span>

```py
print "Hello, World!";
```

Save this file and open up the terminal. Enter the following command:

```console
$ fxlang helloWorld.fx
Hello, World!
```

Regardless of your OS, the string `Hello, World!` should print to the terminal. 

Voilà, You have written your first fxlang program. Go add that to your resume - fx programmer.

## Deep Dive into the Code
f(x) interpreter executes scipts starting at the top of the file, hence it does not require any `main()` function or an entry point. 

The only line in the file does all the work i.e it prints the string `Hello, World!` to the standard output. There are a few things to notice here,

Firstly, `print` is a _Native IO_ function implemented alongside the core of the interpreter. 

In addition to it, you see `"Hello, World!"` string. We pass the string as an arguement to `print`, and the string is printed to the screen.

Lastly, we end the line with semicolon `;` , which marks the end of expression and for this particular file marks the EOF. Every statement in fxlang ends with a semicolon.

Like other dynamic languages such as Ruby, Python or JS, fxlang is also an interpreted language and does not require to generate a compiled binary. Hence, we see the output directly on the stdout.

## Try more out of `print` function
To explore more, try printing out a sum of 2 numbers for example, `(1+1)`. [HINT] I already gave one. 
