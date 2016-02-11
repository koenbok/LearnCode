# Programming

### Programming is hard because

- Mix between English, logic and math.
- It is very strict: tabs, spaces, commas and capitalization matters.
- Errors can be hard to understand but often mean something simple.

### Before we begin

- You can display results with `print 123`.
- Errors appear in the bottom and you can dive deeper with inspector.

### Values and types

- Numbers: `10`, `0.0283`, precision.
- Strings: `"a"`, `"Koen is nice."`, `"412"`.
- Booleans: `true` or `false`, or actually just `1`, `0`. There are more subtypes like this.

### Operators

Things that change values, like math: `+-/*`.

- `print 10 + 10`
- `print 10 / 10`
- `print "a" + "b"`
- `print "a" + 10`, pretty nonsensical, right? It _changes_ your value type.

### Variables

Variables is just assigning a name to a value so you can use it anywhere and as often as you like. It's like `x = 10` in math, but in programming you may use full words (without spaces or special characters) but keep them simple like: `name = "Koen"`. If you need multiple words you'll often see things like `personName = "Koen"`.

Let's write a program that displays my name and age ten years from now.

`print "Koen will be " + (33 + 10) + " in 10 years from now."`

Notice we use 10 twice. Let's convert this into a program we can use for anyone by using variables.

```
name = "Koen"
age = 33
years = 10

print name + " will be " + (age + years) + " in " + years + " from now."
```

Change the variables and see different output.

### Structures: Array and Dictionary

Something we pretty commonly do is making lists of things. These are called Arrays in programming. Let's invent it.

```
1. Koen
2. Jorn
3. Sara
```

- What could you do to a list (add, remove).
- How would you add an item to this list?
- How would you remove an item from this list? Aha, you need its number. We call these an index in programming.
- How would you get an item from the list. Yep you need the same number.

- Ok. Now let's actually do it. Create an Array like `people = ["Koen", "Jorn", "Sara"]`.
- Read an item from the list with an index `print people[1]`. Why would you get this result? Computers count from 0.
- Add an item with `push` like `people.push("Ben")`.
- Delete an item with `delete` like `delete people[0]`.

Also note you can say things about the list in aggregate. Like the length or you can re-order it because lists are sorted.

Now, we will invent a dictionary. They basically only have one difference, let's see if you can figure it out. Assume you have a list of first and last names, like above, and you need to look things up by last names. What would that change?

Indeed, you'll want to use the last name as an index (or a string instead of a number, right?). We call these keys. The notation is as follows:

```
people = {
    bok: "Koen",
    dijk: "Jorn",
    suhr: "Sara"
}
```

- How would you read an item? `people["bok"]`
- How would you delete an item? `delete people["bok"]`

### Input and output

Before we dive in deep with functions let's take a step back. In computers we talk a lot about I/O, or input output. Input can be anything but is most often things like a keyboard. Output can be a screen or a printer. Can you think of anything more?

But I/O doesn't just work on that level, it works on every level. For example your hard drive also provides I/O, just like your network. So basically putting things in and getting stuff out is all that computers are about.

### Function

At the smallest level, a mathematic formula has inputs and outputs too, can you discover them?

`x = y + 100`

A function is the exact same thing. But the notation is as follows. Again, can you spot the inputs and outputs.

```
x = (y) ->
    return y + 100

print x(100)
print x(20)
```

Notice how you can add as much code as you like in the function body, and that you can re-use it as often as you want. Now, as an exercise let's put our name and age calculation program in a function. Given the following, can you finish the function body and use it for a few different values?

```
program = (name, age, years) ->
    return …

```

Congratulations, you just wrote your very first computer program.

### Logic

Logic allows you to only do things on certain condition. It uses the `if` and `else` keywords.

```
if name == "Koen"
    print "His name is Koen"
else
    print "His name is not Koen"
```

### Loops

For items in structures you often want to do something to every item in a list.

```
for item in people
    print item
```
