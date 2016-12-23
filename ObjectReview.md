## Intro to objects
Objects are essentially lists of key/value pairs.

Objects are similar to arrays, except each value in an object has an explicit 'key', instead of an index.

We can access object values by their keys by using either 'dot' notation or brackets.

Object examples:
```js
var usernamesAndPasswords = {nsync4lyfe: "xsdw33", ledzeppelin279: "zep745", boring_username: "df3rds", jimbo233: "uwe9292"}

console.log(usernamesAndPasswords.boring_username);
console.log(usernamesAndPasswords["boring_username"]);

```

```js
var favoriteFoods = {john: "ice cream", sarah: "steak", liz: "pizza"}
```

## Demo: Intro to objects
- Defining an object using brackets
- Accessing properties in objects using both dot notation and brackets
- Different types of object keys (i.e. strings, variables, numbers)
- 'Methods' and storing functions in objects
- Looping over objects
- Math object

## Arrays vs Objects
**Discussion** What’s are the differences between arrays and objects? What are some situations where we should use an array instead of an object? Vice versa?


### Q1. iObject

Create an object that has some information about yourself, including your name, hometown, favorite food, and favorite musical artist. Feel free to add any other properties you'd like.

 ```js
var nate = {name: 'Nate',
            hometown: 'Montclair, NJ',
            favorite_food: 'Chocolate ice cream',
            favorite_artist: 'Jimi Hendrix'}
```

### Q2. create-object

Create an object called `company`. The company object should contain the following properties: name, year founded, CEO. The CEO should be an object that contains two properties: `name` and `age`. Choose a real company (other than Apple) and add its details.

Example:
```javascript
{ name: 'Apple', founded: 1976, ceo: { name: 'Tim Cook', age: 55 } }
```
### Q3. get-object-name

Write a function named `getObjName` that takes in an object as an argument. The function return the value of the `name` property of the object.

Examples:
```javascript
getObjName({name: 'Jimi', insrument: 'guitar'});  // returns 'Jimi'
getObjName({name: 'Snorlax', type: 'normal'});  // returns 'Snorlax'
```

### Q4. favorite-movies

 (a) Create an array of 3-5 objects, where each object describes one of your favorite movies and has properties for the `title`, `genre`, and `year_released`.
 (b) Make a function that logs the first movie's `year_released`
 (c) Make a function that uses `forEach` to log each movie's `year_released` 

### Q5. javascript-simple-objects-2

Create two objects:
1. An object called **whiteRabbit**, containing as property a variable named **type**. Make this variable equal to *white*.
2. An object called **fatRabbit**, also containing as property a variable named **type**. Make this variable equal to *fat*.

Write a function called **whatKindOfRabbit** which accepts as an argument an object called **rabbit**. Make the function log to the console the *type* property of the object, like this:


```
This is a ______ rabbit
```

### Q6. javascript-simple-objects-3

Create two objects:
1. An object called **cat**. This object will contain the properties **kind** ("cat") and **age** (2);
2. An object called **mouse**. This object will contain the properties **kind** ("mouse") and **age** (20);

Write a function called **whoIsWiser** that accepts two objects as arguments: **firstAnimal** and **secondAnimal**. Have the function compare the **age** property of the two objects. If the age is equal, it
will print out
```
These two are equal in wisdom.
```
 If the age is not equal, it will print out:

```
The [older animal] is wiser than the [younger animal]
```

Call the function with the following variables:
1. mouse, cat.
2. cat, mouse.
3. cat, cat.
4. mouse, mouse.

### Q7. javascript-simple-objects-4

You are given the following code:
```javascript
var mouse = {
    name: "French Mouse",
    words:[ "Would YOU like cats if you were me?",
          "As if I would talk on such a subject! Our family always HATED cats: nasty, low, vulgar things! Don't let me hear their name again!",
          "Nothing. The mouse is leaving."]
}

var girl = {
  name: "Alice",
  words: [ "Oh, I beg your pardon! I quite forgot you didn't like cats. ",
         "Well, perhaps not. We won't talk about cats any more if you'd rather not.",
         "I won't indeed! Are you--are you fond--of--of dogs?"]
}
```

write a function called **dialogue** that would accepts as arguments two objects, **speaker1** and **speaker2**. Inside the function, log to the console **words** arrays of both speakers as follows:


- [ speaker 1's **name** ] + " says " + [ speaker1's **words[0]** ]
- [ speaker 2's **name** ] + " says " + [ speaker2's **words[0]** ]
- [ speaker 1's **name** ] + " says " + [ speaker1's **words[1]** ]
- [ speaker 2's **name** ] + " says " + [ speaker2's **words[1]** ]
- ...

Assume that both **words** arrays are of the same length. However, you do not know the length of these arrays in advance.

### Q8. javascript-simple-objects-1

Create an empty object called **rabbit**. Add a function called **speak** as a property to your object. This function will accept a single argument and log to the console "The rabbit says: " followed by the argument. Call the function with the string "Can I have some lettuce?".

The output should look like this:
```
The rabbit says: Can I have some lettuce?
```
### Q9. obj-length

Write a function called `objSize` that takes this object as its input and return the object's size (number of properties in the object) as its output.

Example:
```js
var student = {
  name : "Tony Stark",
  university: "MIT",
  Major: "Physics",
  age : 40
};

objSize(student); //returns 4
```
### Q10. javascript-simple-objects-5

You are helping create a simple text-based role playing game. The Following code is given:

```javascript
var player1 = {
    name: "Player",
    attack: 2
}

var monster1 = {
    name: "Goblin",
    hp:10,

   /*
    *    Call this function when the monster gets hit. It will log the monster's remaining hp to the console
    *    @arg damage - the number to be substracted from the monster's hp
    */
    gotHit: function(damage){
        // If damage would bring hp to less then zero, setting hp to zero
        this.hp = (this.hp - damage >= 0) ? (this.hp - damage) : (0);
        // Printing out how much hp the monster has left
        console.log(this.name + " has " + this.hp + " hp");
    },
    // Call this function to check if the monster is dead
    isDead: function(){
        return this.hp === 0;
    }
}
```

Write a new function `fight(player, monster)`

In this function, the player will hit the monster until it is dead. Before each hit, log to the console:
```
[The player's name] hit [the monster's name]
```
 When the monster is dead, log to the console:
```
[The monster's name] has been defeated
```

Use the given functions of **monster1**.


[source](https://github.com/C4Q/AC3.1/tree/master/lessons/javascript-fundamentals/objects-and-arrays)


# Resources
- [W3 JavaScript Intro to Objects](http://www.w3schools.com/js/js_objects.asp)
- [Working With Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
