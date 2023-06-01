# Typescript: Type

- [`omit`](#omit)
- [`pick`](#pick)

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


### `pick`

to create a new type by picking the specific property from existing type

```typescript
interface Person {
  name: string;
  age: number;
  email: string;
}

type PersonNameAndAge = Pick<Person, 'name' | 'age'>;

const person: PersonNameAndAge = {
  name: 'John',
  age: 30,
};
```

[↑ top](#typescript-type)
<br><br><br><br><hr>
