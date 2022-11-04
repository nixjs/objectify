# @nixjs23n6/objectify

A tiny object utility.

## Quick Setup

### Install

`yarn add @nixjs23n6/objectify`

### Usage

#### Rename keys

```typescript
const obj = { id: 'toto_id', name: 'toto', age: 35 }
const keys = { id: 'value', name: 'label' }

renameKeys(keys, obj)
// { "value": "toto_id", "label": "toto", "age": 35 } 
```

#### Merge

```typescript
const obj1 = {
  a: null,
  b: false,
  c: true
};
const obj2 = {
  k: "demo"
};

merge(obj1, obj2);
// { a:null, b: false, c: true, k: "demo" }
```

#### Omit

```typescript
const obj = {
  a: null,
  b: false,
  c: true
};

omit(obj, ['a','b']);
// { c: true }
```

#### Pick

```typescript
const obj = {
  a: null,
  b: false,
  c: true
};

pick(obj, ['a','b']);
// { a: null, b: false }
```

#### Compact

```typescript
const obj = {
  a: null,
  b: false,
  c: true,
  d: 0,
  e: 1,
  f: '',
  g: 'a',
  h: [null, false, '', true, 1, 'a'],
  i: { j: 0, k: false, l: 'a' }
};

compact(obj);
// { c: true, e: 1, g: 'a', h: [ true, 1, 'a' ], i: { l: 'a' } }
```
