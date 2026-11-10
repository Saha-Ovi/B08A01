Type Aliases vs Interfaces in TypeScript
Type Aliases vs Interfaces in TypeScript

When starting out with TypeScript, choosing between type aliases and interfaces can feel confusing because both let us define object structures. However, understanding their core differences helps us write cleaner and more maintainable code.

The main difference lies in how they handle extensions and declarations. Interfaces are open for extension, meaning you can declare the same interface multiple times and TypeScript will merge them automatically through declaration merging. In contrast, a type alias cannot be reopened to add new properties once created. Additionally, type aliases are more flexible because they can represent primitives, unions, and tuples, whereas interfaces are strictly for describing object shapes.

// Interface example with declaration merging

interface User {
    name: string;
}
interface User {
    age: number;
}

// Type alias example using union types

type Status = "pending" | "approved" | "rejected";
type Role = { role: string };
type AdminUser = User & Role;


So, when should you use which? As a general rule of thumb, use interfaces when you are building object-oriented code, library contracts, or public APIs where consumers might need to extend types. Choose type aliases when working with union types, primitives, tuples, or complex function signatures. Mastering both gives you full control over your TypeScript projects.