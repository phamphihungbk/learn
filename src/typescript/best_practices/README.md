# Typescript: Best Practices

- [`any vs unknown`](#any-vs-unknown)

[↑ top](#typescript-best-practices)
<br><br><br><br><hr>

### `any vs unknown`

- use unknown instead in case don't know type of variable

```typescript
interface IUser {
    id: number;
    name: string;
}

interface IAdminUser extends IUser{
    token: string;
}

function isAdminUser(object: unknown): object is IAdminUser {
  if (object !== null && typeof object === "object") {
    return "token" in object;
  }

  return false;
}

async function fetchUser() {
    const response = await fetch('https://api');
    
    // bad
    const badUser: any = await response.json();
    
    // good
    const goodUser: unknown = await response.json();
}
```

[↑ top](#typescript-best-practices)
<br><br><br><br><hr>
