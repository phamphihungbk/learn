# Typescript: Type

- [`Omit`](#omit)
- [`Pick`](#pick)
- [`Parameters`](#parameters)
- [`ReturnType`](#returnType)

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

### `parameters`

a utility to obtain the parameter types of a function or constructor as a tuple type

```typescript
function greet(name: string, age: number): void {
  console.log(`Hello, ${name}! You are ${age} years old.`);
}

type GreetParams = Parameters<typeof greet>; // [string, number]

const params: GreetParams = ['Alice', 25];
greet(...params); // Hello, Alice! You are 25 years old.
```

[↑ top](#typescript-type)
<br><br><br><br><hr>


### `returnType`

a utility to extracts and represents the return type of function

```typescript
function greet(): string {
  return 'Hello!';
}

type GreetReturnType = ReturnType<typeof greet>;
// The type GreetReturnType is inferred as string

const greeting: GreetReturnType = greet();
// The variable greeting is inferred as string

function add(a: number, b: number): number {
  return a + b;
}

type AddReturnType = ReturnType<typeof add>;
// The type AddReturnType is inferred as number

const sum: AddReturnType = add(5, 3);
// The variable sum is inferred as number
```

[↑ top](#typescript-type)
<br><br><br><br><hr>
