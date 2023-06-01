# Typescript: Type

- [`omit`](#omit)

[↑ top](#typescript-type)
<br><br><br><br><hr>

### `omit`

to create a new type to exclude the specific property from existing type

```typescript
interface Person {
  name: string;
  age: number;
  address: string;
}

// Exclude the 'address' property from the 'Person' type
type PersonWithoutAddress = Omit<Person, 'address'>;

// Usage
const person: PersonWithoutAddress = {
  name: 'John',
  age: 30,
};
```

[↑ top](#typescript-type)
<br><br><br><br><hr>
