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
let updatedFruit = {
  id: 1, 
  name: "apple pie"
};

fruits = Object.keys(fruits).reduce((previous, key) => {
  if (key == updatedFruit.id) {
    previous[updatedFruit.id] = updatedFruit;
  } else {
    previous[key] = fruits[key];
  }
  return previous;
}, {})

// {1: {id: 1, name: "applie pie"}, 2: {id: 2, name: "pear"}}
```

### Delete

```javascript
let deleteById = 1;

fruits = Object.keys(fruits).reduce((previous, key) => {
  if (key != deleteById) {
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
```javascript
let updatedVegetable = {
  id: 1, 
  name: "carrot juice"
};

vegetables = vegetables.map(vegetable => {
  if (vegetable.id === updatedVegetable.id) {
    return updatedVegetable;
  } else {
    return vegetable;
  }
});

// [{id: 1, name: "carrot juice"}, {id: 2, name: "lettuce"}]
```

### Delete
```javascript
let deleteById = 1;

vegetables = vegetables.filter(vegetable => {
  return vegetable.id !== deleteById;
});

// [{id: 2, name: "lettuce"}]
```