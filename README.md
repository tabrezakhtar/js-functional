# Useful JavaScript snippets

## Functional programming

Construct a new object with reduce

```
const allItems = ['item1', 'item2', 'item3', 'item4', 'item5', 'item6'];
const selected = { item2: 2, item4: 2, item6: 1 };

const result = allItems.reduce((acc, item) => ({
	...acc,
	[item]: selected[item] ? selected[item] : 0,
}), {})

console.log('func',result)
```

Flatten an array of items with reduce and Set

```
export const flattenItems = (items) => {
  const result = items.reduce( (prev, next) => prev.concat(next.subItems), []);
  return [...new Set(result)];
}
```

Total items with reduce

```
items.reduce((acc, item) => acc + item.price, 0);
```

Unique values using Set

```
let uniqueArray = [...new Set([5,5,2,4,2])];
```