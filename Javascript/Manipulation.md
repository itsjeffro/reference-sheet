# Manipulating objects and arrays

[Manipulating objects](#manipulating-objects)

- [Add to object](#add-to-object)
- [Update property value](#update-property-value)
- [Remove from object](#remove-from-object)


[Manipulating arrays](#manipulating-arrays)

- [Add object in array](#add-object-in-array)
- [Update object in array](#update-object-in-array)
- [Remove object from array](#remove-object-from-array)

---

## Manipulating objects

Given that our starting object is the following...
```javascript
let fruits = {
  1: {id: 1, name: "apple"}
};
```

### Add to object

```javascript
let fruit = {
  id: 2,
  name: "pear"
};

fruits = {
  ...fruits,
  [fruit.id]: {fruit}
};
```
```javascript
{
  1: {id: 1, name: "apple"},
  2: {id: 2, name: "pear"}
}
```

### Update property value

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
```
```javascript
{
  1: {id: 1, name: "apple pie"},
  2: {id: 2, name: "pear"}
}
```

### Remove from object

```javascript
let deleteById = 1;

fruits = Object.keys(fruits).reduce((previous, key) => {
  if (key != deleteById) {
    previous[key] = fruits[key];
  }
  return previous;
}, {})
```
```javascript
{
  2: {id: 2, name: "pear"}
}
```

## Manipulating arrays
Given that our starting array is the following...
```javascript
let vegetables = [
  {id: 1, name: "carrot"}
];
```

### Add object in array
```javascript
vegetables = vegetables.concat({id: 2, name: "lettuce"});
```
```javascript
[
  {id: 1, name: "carrot"},
  {id: 2, name: "lettuce"}
]
```

### Update object in array
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
```
```javascript
[
  {id: 1, name: "carrot juice"},
  {id: 2, name: "lettuce"}
]
```

### Remove object from array
```javascript
let deleteById = 1;

vegetables = vegetables.filter(vegetable => {
  return vegetable.id !== deleteById;
});
```
```javascript
[
  {id: 2, name: "lettuce"}
]
```
