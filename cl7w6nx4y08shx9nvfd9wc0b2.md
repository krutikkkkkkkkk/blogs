## All you need to know about JSON?

# What is JSON?

JSON stands for **JavaScript Object Notation**

It is an open standard file format and data exchange format that employs text that humans can read to store and send data objects made up of attribute-value pairs and arrays (or other serializable values). It is a widely used data format for electronic data exchange, notably between servers and online applications.

JSON file is saved with *.json* xxtension.

# JSON Types
1. Strings : `"Krutik Raut"` `"Hello World"`
2. Numbers:  `13`  `0.6`   `-21`
3. Booleans: `true` `false`
4. Arrays : `[1,2,3]` `["Hi", "Hashnode"]`
5. Objects: `{"key":"value", "name": "Krutik"}`

Note: **JSON names require double quotes. JavaScript names do not.**

# JSON Syntax

1. Data is in name/value pairs
2. Commas are used to separate data
3. Curly braces hold objects
4. Square brackets hold arrays

**Example: **

```
{
    "name":"Krutik", 
    "age":20 , 
    "isDeveloper": true,
    "languages": ["HTML","CSS","JavaScript","PHP"],
    "Idk":null,
    "pets":[{"name": "Robert","type" : "Dog"},
                {"name": "Max", "type" : "Cat" }]
}

```

# How to access data from a JSON file or Object?

If we load this data as a variable called **info**, we could then access the data inside it using the same dot/bracket notation.
For example:


`info.name` or `info['name']`

Output: 
```
"Krutik"
```


`info.pets[1].name`

Output: 
```
"Max"
```

`info.languages[2]`

Output: 
```
"JavaScript"
```


# Why use JSON?

The syntax of the JSON format is similar to that of the JavaScript object creation code. This makes it simple for a JavaScript code to turn JSON data into JavaScript objects.

JSON data may be used in any programming language and is easily transferable between machines because it is merely in text format.

### Things to keep in mind while writing JSON

1. JSON consists solely of a string with a predefined data format.It has no methods,only properties.
2. JSON requires double quotes to be used around strings and property names. Single quotes are invalid.
3. A single missed comma or colon might cause a JSON file to stop working.






