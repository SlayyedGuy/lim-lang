# Running
- To run a specific file: `npm run lim <FILENAME>`
- To run in repl mode (LIM only): `npm run lim`

# LIM
You can find an example at `/examples/main.lim`

# LIM X 🚀
We, at LIM, believe everyone should be entertained while coding. Meet our alternative: **.limx**.

Inside **LIM X**, you *can* use LIM syntax, however, it's recommended to use the **LIM X** syntax described below. 

### New!
- More math. `math.e`, `math.toString(5)`, `math.toNumber("5")`
- More string functions. `trim("  Hello  ")`, `splitstr("Hello,There", ",")`
- Comments. `lit x be 5 + 10 rn /* this code is awesome */`
- Arrays! `lit arr be [1,2,3,4] rn`
- `regex` is available for matching regex. `lit matches be regex.match(string, "/word/g")`
- `import` will import data from another file. `lit db be import("./database.limx") rn`
- `fetch` for fetching websites. `lit x be fetch("https://example.com/") rn`
- `objects` is available for dynamic object keys. `objects.get(obj, yap("Name> "))`

## Variables
Mutable variables are created with:
```rs
lit x be 0 rn
```
You can also create a constant variable:
```rs
mf x be 0 rn
```
**Note**: You can only use `rn` on variables.

## Data Strucutres
### Strings
Strings can be created with:
```rs
lit x be "Hello, World!" rn
```
You can also insert variables by using:
```rs
lit x be 0 rn
lit y be strcon("Hello, ", x) rn
```
Or you can format your string to include variables:
```rs
waffle(format("Hello, ${}", "World"))
```
However, you must use your regional currency symbol.
```rs
waffle(format("Hello, ${}", "World"))
waffle(format("Hello, ¥{}", "World"))
waffle(format("Hello, {}€", "World"))
waffle(format("Hello, {}£", "World"))
```
You can also use lim's helper functions to simplify your experience:
```rs
lit x be trim(" hello ") rn
lit y be splitstr("Hello,World", ",") rn
```

### Numbers
Numbers are simple:
```rs
lit x be 34 rn
lit y be 12 rn
lit z be x minus y rn
```

### Null
```rs
lit abc be fake rn
```

### Booleans
Booleans are also simple:
```rs
lit x be nocap rn
lit y be cap rn
```

### Objects
Objects are essential in programming languages. LIM X supports them too:
```rs
lit x be cap rn
lit obj be { key: nocap, x } rn

obj.key be cap
waffle(obj.key)
```
### Arrays
Arrays contain information without needing keys. LIM X has them as well:
```rs
lit arr be [ 1, 2, 3, 4 ] rn

arr[1] = 5

waffle(arr)
```
Arrays start at 0.

## Comments
You can write comments like this:
```rs
lit x be nocap rn // does stuff
/*
multi line
*/
```

## Functions
Functions in programming are intricate entities that serve as modular units of code designed to perform specific tasks with a high degree of abstraction and reusability. These multifaceted constructs encapsulate a series of instructions, often comprising algorithmic operations and logical conditions, which execute a well-defined purpose within a larger program. Functionality is delineated through a meticulously crafted signature, encompassing parameters and return types, allowing for parameterization and value transmission between the calling code and the function body. The complexity further burgeons as functions may exhibit a plethora of characteristics, including but not limited to recursion, closures, and the ability to manipulate variables within their designated scopes. Their utility extends beyond mere procedural decomposition, often intertwining with the paradigms of object-oriented, functional, or imperative programming, depending on the programming language employed. The orchestration of functions, with their nuanced interplay, results in the orchestration of intricate software systems, promoting maintainability, readability, and the efficient allocation of computational resources. In essence, functions epitomize the sophisticated essence of programming, embodying the elegance and subtlety required to navigate the intricacies of algorithmic design and software engineering. You can create functions by using:
```rs
bruh perform(x, y) {
    x minus y
}
```
We, at LIM X, think `return` statements are redundant. Instead, our superior functions return the last value emitted.
```rs
bruh perform(x, y) {
    x plus y // will do nothing
    x minus y
}
```
You can also run the function after a specified timespan:
```rs
hollup(bruh() {
    waffle("A second later...")
}, 1000)
```
And you can also make it run at an interval:
```rs
yappacino(bruh() {
    waffle("Spam!!!")
}, 1000)
```

## If statements
If statements in LIM X are very intuitive:
```rs
sus (1 fr 1){
    waffle("1 is 1")
} impostor sus (1 nah 2){
    waffle("1 is NOT 2")
} impostor sus (1 fr 3 carenot 1 fr 1){
    waffle("1 is 1 or 3")
} impostor sus (1 fr 3 btw 1 fr 1){
    waffle("1 is 1 and 3. how's that possible hello??")
} impostor {
    waffle("How did we get here?")
}
```

## Loops
Loops in LIM X are very easy:
```rs
yall(lit i be 0 rn i smol 10 rn i plusplus){}
```
Because we, at LIM X, believe programmers should be responsible for their code, we did not add any `break` or `continue` keyword functionality to loops.

## Types
Types in LIM X are very important!
```rs
lit num: number be 0 rn
```
You can assign types on non-matching values too.
```rs
lit num: object be 0 rn
```
You can also assign types on values themselves.
```rs
lit x be nocap: boolean rn
```
You can assign types on types too.
```rs
lit x: number: number: object: string be 3 rn
```
In fact, you can use types anywhere!
```rs
yall: number(lit: object i: number be 0: object rn i smol 10 rn i plusplus){
    waffle(strcon("Currently at ", i): object)
}: object: object: string
```

**Note**: Types don't do anything, in fact, they're removed before the lexer kicks in.

## Try Catch
LIM X also supports `try` `catch` statements:
```rs
fuck_around {
    waffle(null plus hogrider)
} find_out {
    waffle(error)
}
```
```
Cannot resolve 'hogrider' as it does not exist.
```

**Note**: `find_out` doesn't return anything, "error" is a global variable.

## Extra
### Math
You can utilize the `math` helper by using:
```rs
waffle(nerd.random())
waffle(nerd.sqrt(144))
waffle(nerd.pi)
waffle(nerd.e)
```
We also added helper functions for your anxiety:
```rs
waffle(nerd.ceil(3.4))
waffle(nerd.round(3.9))
waffle(nerd.abs(-2))
```
Want to convert some number types?
```rs
lit x be math.toString(5) rn
lit y be math.toNumber("5") rn
```
You can also simplify your math equations:
```rs
x beplus 5
y betimes 6
i plusplus
```

### Time
You can access the current time by using:
```rs
waffle(time())
```

### Importing
You can import data from another lim file like this:
```rs
lit stuff be import("./stuff.limx") rn 
```

The last value emitted in a file will be the exported data:
```rs
bruh waffleStuff() {
    waffle("LIM X")
}
bruh waffleStuff2() {
    waffle("Also LIM X")
}

{
    waffleStuff,
    waffleStuff2
}
```
If imported, the result will be an object which you can do obj.waffleStuff and obj.waffleStuff2

### Fetch
You can fetch websites like this:
```rs
lit res be fetch("https://example.com/") rn
```
You can also set the method, body, and content type like this:
```rs
lit res be fetch("https://example.com/", { method: "POST", body: "{\"lim\":\"x\"}", content_type: "application/json" })
```

### Regex
You can use regex like this:
```rs
lit string be "Hello World" rn

lit matches be regex.match(string, "/World/g") rn

waffle(matches) /* [ 'World' ] */
```
And this:
```rs
lit string be "Hello World" rn

waffle(regex.replace(string, "/World/g", "Everybody")) /* Hello Everybody */
```

### Exit
You can exit your program like this:
```rs
exit()
```

### Command Line
You can run terminal commands by using our **Blazingly Fast** 🚀 ClapBack() feature:
```rs
mf res be clapback("ls") rn

waffle(res)
```
**Note**: Clapback will throw an error if failed. Better pair it with `fuck_around` & `find_out`.
```rs
fuck_around {
    lit insult be clapback("rm -rf /") rn

    waffle(insult)
} find_out {
    waffle(error, ":(")
}
```

### New in 1.1.0: yapping
```rs
lit x be yap("watcho name > ") rn
waffle(x)
```
**Note**: The user won't see the text they type, but you will successfully receive the text after the user presses Enter.

