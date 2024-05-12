# Optional Properties in TypeScript Interfaces

In TypeScript, you can make properties optional in an interface by using the `?` syntax after the property name. This allows you to define interfaces where certain properties may or may not be present in objects that implement the interface.

## Syntax

The syntax for defining optional properties in an interface is as follows:

```typescript
interface User {
    id: number;
    name: string;
    age?: number; // Optional property
    email?: string; // Optional property
}
