# Type Aliases vs Interfaces in TypeScript

TypeScript provides two ways to define custom types: `type` aliases and `interface`. Both help developers define object structures and improve code readability and type safety. However, they have some important differences.

### 1. Interface

An `interface` is mainly used to define the structure of an object.

```typescript
interface Employee {
    id: number;
    name: string;
    salary: number;
}

const employee: Employee = {
    id: 1,
    name: "Rakib",
    salary: 50000
};
```

Interfaces can also be extended using the `extends` keyword to reuse properties from another interface.

### 2. Type Alias

A `type` alias allows us to create custom names for different types, including objects, strings, numbers, unions, and tuples.

```typescript
type Status = "Pending" | "Approved" | "Rejected";

type Employee = {
    id: number;
    name: string;
};
```

Unlike interfaces, type aliases can directly support union and intersection types.

### 3. Core Differences

The main difference is that interfaces are mainly designed for defining object structures, while type aliases can represent almost any TypeScript type.

Interfaces support declaration merging, meaning multiple declarations with the same name can be combined. However, type aliases cannot be declared multiple times with the same name.

Interfaces use the `extends` keyword to inherit properties, whereas type aliases use the intersection (`&`) operator to combine multiple types.

### 4. When to Use Them

Use `interface` when defining object structures, class contracts, and reusable APIs. Use `type` when working with union types, intersection types, tuples, and primitive types.

### Conclusion

Both are useful in TypeScript. Interfaces are generally preferred for defining object structures, while type aliases provide more flexibility for creating complex types. The choice depends on project requirements and coding preferences.