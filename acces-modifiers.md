Understanding Access Modifiers in TypeScript OOP

Object-Oriented Programming (OOP) in TypeScript allows us to control how properties and methods are accessed outside a class. We achieve this control using access modifiers: public, private, protected, and readonly.

By default, every property or method in a class is public. This means anyone can read or modify it from anywhere. If you want to hide sensitive data like account numbers or passwords, use private. Private properties can only be accessed within the class itself. When you want child classes to access parent properties while still hiding them from the outside world, use protected. Finally, the readonly modifier prevents properties from being modified after initialization.

class Account {
    public holder: string;
    private balance: number;
    protected accountType: string;
    readonly id: number;

    constructor(holder: string, balance: number, id: number) {
        this.holder = holder;
        this.balance = balance;
        this.accountType = "Savings";
        this.id = id;
    }

    public getBalance(): number {
        return this.balance; // Allowed inside the class
    }
}


Using access modifiers effectively helps keep your code secure and organized. They prevent accidental data modification and create clear boundaries between different parts of your application, making your codebase much safer and easier to maintain.