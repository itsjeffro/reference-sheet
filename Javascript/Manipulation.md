# Manipulating objects and arrays

## Objects

Given that our starting object is the following...
```javascript
let fruits = {
  1: {id: 1, name: "apple"}
};
```

### Add

```javascript
let fruit = {
  id: 2,
  name: "pear"
};

fruits = {
  ...fruits,
  [fruit.id]: {fruit}
};

// {1: {id: 1, name: "apple"}, 2: {id: 2, name: "pear"}}
```

### Update

```javascript
let fruit = {
  id: 1, 
  name: "apple pie"
};

fruits = Object.keys(fruits).reduce((previous, key) => {
  if (key == fruit.id) {
    previous[fruit.id] = fruit;
  } else {
    previous[key] = fruits[key];
  }
  return previous;
}, {})

// {1: {id: 1, name: "applie pie"}, 2: {id: 2, name: "pear"}}
```

### Delete

```javascript
let id = 1;

fruits = Object.keys(fruits).reduce((previous, key) => {
  if (key != id) {
    previous[key] = fruits[key];
  }
  return previous;
}, {})

// {2: {id: 2, name: "pear"}}
```

## Arrays
Given that our starting array is the following...
```javascript
let vegetables = [
  {id: 1, name: "carrot"}
];
```

### Add
```javascript
vegetables = vegetables.concat({id: 2, name: "lettuce"});

// [{id: 1, name: "carrot"}, {id: 2, name: "lettuce"}]
```

### Update
TBA

### Delete
TBA