# Type Aliases vs Interface in TypeScript

## Introduction

TypeScript provides two important features for defining custom data structures: `type` aliases and `interface`. Both help developers describe the shape of data and make code more organized. Although they look similar, they have some differences in their features and usage.

## What is a Type Alias?

A `type` alias allows us to create a custom name for any type. It can define objects, primitive types, union types, tuples, and more. For example, we can use a type alias to define the structure of a user.

```typescript
type User = {
  name: string;
  age: number;
};

const user: User = {
  name: "Rafi",
  age: 20,
};
```

One useful feature of `type` is that it supports union (`|`) and intersection (`&`) types.

## What is an Interface?

An `interface` is mainly used to define the structure of objects. It describes which properties and methods an object should have. Interfaces make object structures easier to understand and maintain. We can also extend an existing interface using the `extends` keyword.

```typescript
interface Person {
  name: string;
}

interface Employee extends Person {
  salary: number;
}
```

## Main Differences Between Type and Interface

Both `type` and `interface` can define object structures. However, `type` is more flexible because it supports primitive, union, intersection, and tuple types. An `interface` is mainly focused on object structures. Another important difference is declaration merging. Interfaces with the same name can be automatically combined, but type aliases do not support declaration merging.

## When Should We Use Them?

We should use `interface` when defining object structures or creating class contracts. We should use `type` when working with unions, intersections, tuples, or complex type combinations.

## Conclusion

Both features are useful and help us write clean and type-safe TypeScript code. Choosing between them depends on the project requirements and the type of structure we want to define.