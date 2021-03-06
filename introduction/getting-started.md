# Getting Started
The secret to getting ahead is getting started. In this section we will get our hands dirty by learning about variables, constants and simple data types.

## Variables
Variables can be considered as the places where we can store program data. They are called variables because their values can vary. You are free to change their values.

Now lets launch XCode app, and it will ask you what you want to do. 
* Choose "Get started with a Playground" (This is a play area for your codes where you can play with your swift codes for testing purpose and here you can see immediate results unline in Xcode IDE where you need actual device or simulator to see your output.)
* Choose "blank" and click "next" and create to save it whereever you like. For example save it to your desktop. 

In your playground area, you will see a line of code

```swift
var str = "Hello, playground"
```

```
Output: Hello, playground
```

This creates a new variable called ``str`` with the value ``Hello, playground``. You can see the output as ``Hello, playground`` in the right side. 

As the name suggests, we can change the value of ``str`` because it is a variable.

```swift
str = "Hello, world!"    
```

```
Output: Hello, world!
```

Now this time we don't need the keyword ```var```, because the variable has already been created and we are just changing its value. 

Similarly if you want to create another variable, just follow the above code with the code below,

```swift
var name = "Sanjay Khadka"
print(name)
```

```
Output: Sanjay Khadka
```

If you have set the playground to run automatically at the bottom side of the playground(also recommended), then you will see the output at the right side of the playground once the execution completes. 

![execute image](https://github.com/sanjaykhadka/learn-swift-coding/blob/master/images/execute.gif)

Here print is used to print the output to the bottom console of the playground.

![Playground Image](https://github.com/sanjaykhadka/learn-swift-coding/blob/master/images/playground.png)

## Strings & Integers
Unline PHP, in swift every variable must have some specific data type, which is why swift is a type-safe language, ie we must assign the variable some specific data type. 

Thus, string is a group of characters placed together and assigned to a variable. We must use double quotes ```" "``` to define a string type variable. 

```swift 
var color = "red"
```

```
Output: red
```

Likewise if we need a variable to store a whole number, we must create a variable like this, 

```swift
var age = 10
```

The variable that stores a numeric value (whole number) without decimals is called an integer type. 

To store the large number, swift lets us use underscore ```_``` as thousand separators.

```swift
var population = 50_000_000
print(population)
```

```
Output:
50000000
```

Because strings and integers are different types, we can't use string to hold integer value and vice versa. 

## Multi-line Strings
Standard swift strings created by using double quotes ```" "``` can't include line breaks and thus can't store multiple line string values. To create multi-line string, use three double quote marks,

```swift
var sentence = """
Ram and
Shyam are
friends
"""
print(sentence)
```

```
Output: 
Ram and
Shyam are
friends
```

But if you don't want the actual line breaks ```\n``` in your string output (in the case where you need to store long sentences but using multi-line just to format your code in XCode editor), use ```\``` at the end of ech line. 

```swift
var sentence1 = """
Ram and \
Shyam are \
friends
"""
print(sentence1)
```

```
Output: 
Ram and Shyam are friends
```

Now though you are using multi-line to format your line, those line breaks will actually not be included in your output.

## Double & Booleans
Integers can only store whole numbers. We need a double type to store a fractional value. So whenever we create a variable with a fractional value, Swift automatically uses a double type for that variable.

```swift
var pi = 3.1415
```

And to assign a conditional value like ```true``` or ```false```, we use boolean type.

```swift
var isHappy = true
```

## String Interpolation
When we need to place a variable inside a string, we use a process called string interpolation. We use ```\()``` for string interpolation, inside a string.

```swift
var age = 5
var str = "He is \(age) years old"
var str1 = "Ram is small and \(str)"
print(str1)
```

```
Output:
Ram is small and He is 5 years old
```

## Constants
While variable can vary ie we can change its vaue, the alternative to variable is a constant. We can use keyworld ```let``` to define a constant. Constant is used to prevent the accidental replacement of any values. 

In fact in swift we very often use constants rather than variables, unless we specifically want a variable, and whenever a variable is not replaced with another value, XCode suggests us to use ```let```.

```swift
let gender = "Male"
```

When you try to change the value of a constant XCode will give an error.

## Type Inference and Type Annotations
In swift whenever we define a variable or constant like below,

```swift
var name = "Hari"
let age = 20
```

Swift automatically assigns the data type to each of variable and constant based on the type of value they are using. This ability of Swift to infer the datatype is called type inference. 
But if we don't want Swift to decide what to use, and we want to define the type ourself, we can explicitly assign the type for our variables or constants. This is type annotation. It can be done like this:

```swift 
var name: String = "Ram"
let age: Int = 16
let happy: Bool = true
let pi: Float = 3.1415
var population: Double = 50000000000
```



