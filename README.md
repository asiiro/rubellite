# Rubellite

Rubellite is a dictionary data structure built for JavaScript

### Installation

```console
npm i rubellite --save
```

### Usage

#### Instantiating an empty dictionary

```javascript
var dictionary = new rubellite();
```

#### Instantiating a dictionary using an already existing object

```javascript
var obj = { 
    firstProperty: "someData",
    secondProperty: "someOtherData"
};

var dictionary = new rubellite(obj);
```

#### Retrieving the number of items

```javascript
var count = dictionary.count();
```

#### Adding an item

```javascript
dictionary.add("thirdProperty", 123);
```

#### Adding or Replacing an item

```javascript
dictionary.replace("thirdProperty", 456);
```

#### Adding all key values in an object to the dictionary

##### - Overwrite any key values which are already present in the dictionary

```javascript
var obj = { 
    thirdProperty: "abc",
    fourthProperty: 123
};

dictionary.feed(obj);
```

##### - Skip any key values which are already present in the dictionary

```javascript
var obj = { 
    thirdProperty: "abc",
    fourthProperty: 123
};

dictionary.feed(obj, true);
```

#### Checking if an item already exists

```javascript
var exists = dictionary.containsKey("firstProperty");
```

#### Retrieving an item

```javascript
var item = dictionary.seek("firstProperty");
```

#### Removing an item

```javascript
dictionary.remove("firstProperty");
```

#### Retrieving all keys

```javascript
var array = dictionary.getKeys();
```

#### Retrieving all values

```javascript
var array = dictionary.getValues();
```

#### Retrieving all data as a JSON string

```javascript
var data = dictionary.getJson();
```

#### Clearing the Dictionary

```javascript
dictionary.clear();
``` 

#### Recycling the Dictionary

```javascript
var obj = { 
    firstProperty: "someData",
    secondProperty: "someOtherData"
};

dictionary.recycle(obj);
```

#### *Note about JavaScript primitive types*

Utilising objects as values will ensure mutations when accessing the value via the seek function. If you decide to use a primitive type as a value, such as an integer type, updating it after using the seek function will not update the value inside the dictionary, in this case utilise the provided replace function to update the key's value.

## Author

**Michael Cassar** ([michaelcassar.com](https://www.michaelcassar.com)) - [GitHub](https://bit.ly/3Ro9DcW), [NPM](https://bit.ly/3T4aaSz)
