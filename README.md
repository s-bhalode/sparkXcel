# DTO (Data Transfer Objects)


## Overview

This library was created to solve the problem of taking a data model from a datasource and needing to remove, add, merge, or translate the data model to a similar or completely different object. 

There are similar libraries in other languages (DataMapper, DTO(C#), etc). I could never find a solution that allowed me to quickly and easily utilize a couple of different approaches: *projection*, *translation*, and *merging*.

<<<<<<< HEAD
## Getting Started
=======
>>>>>>> c942a96555d08bb3d928c8ac9c224daa63886043


## Projection
There are two simple ways to project (like a SQL SELECT statement) or simplify an object. I found myself deleting the properties on the object, or using libraries such as lodash to restrict the output. I decided to use Lazy.js for performance reasons.

### Only

Given an array of property names, the resulting object will only contain the supplied properties.

**Example**

```js
let Dto = require('dto');
let model = { name: { first: 'Simran', last: 'Bhalode'}, age: 21, gender: 'Female'};

let result = Dto.take.only(model, ['age', 'gender']);
// result = { age: 21, gender: 'Female' }
```

### Without

Given an array of property names, the resulting object will remove any properties supplied.

**Example**

```js
let Dto = require('dto');
let model = { name: { first: 'Simran', last: 'Bhalode'}, age: 21, gender: 'Female'};

let result = Dto.take.without(model, ['name']);
// result = { age: 21, gender: 'Female' }
```




