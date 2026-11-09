# Access Modifiers in TypeScript OOP

Access Modifiers in TypeScript control how class properties and methods can be accessed. They help protect data and make code more organized. TypeScript provides three main access modifiers: `public`, `private`, and `protected`. It also provides `readonly` to prevent changing property values.

### 1. Public

The `public` modifier allows properties and methods to be accessed from anywhere. It is the default modifier.

```typescript
class Employee {
    public name = "Rakib";
}

const emp = new Employee();
console.log(emp.name); // Rakib
```

### 2. Private

The `private` modifier allows access only inside the class where it is declared.

```typescript
class Employee {
    private salary = 50000;

    getSalary() {
        return this.salary;
    }
}

const emp = new Employee();
console.log(emp.getSalary()); // 50000
```

### 3. Protected

The `protected` modifier allows access inside the same class and its child classes.

```typescript
class Employee {
    protected name = "Rakib";
}

class Manager extends Employee {
    getName() {
        return this.name;
    }
}
```

### 4. Readonly

The `readonly` modifier prevents a property from being changed after initialization or constructor assignment.

```typescript
class Employee {
    readonly id = 101;
}

const emp = new Employee();
console.log(emp.id); // 101
```

### Conclusion

Access Modifiers help developers control data access, protect important properties, and write cleaner, safer, and more maintainable TypeScript code.