# Typescript: Generic

- [`default type parameter`](#default-type-parameter)
- [`type parameter constraints`](#type-parameter-constraints)

[↑ top](#typescript-generic)
<br><br><br><br><hr>

### `default type parameter`

there is no longer a need to pass a type to the ResultType generic parameter when calling the fetchApi function

```typescript
async function fetchApi<ResultType = Record<string, any>>(path: string): Promise<ResultType> {
    const response = await fetch(`https://example.com/api${path}`);
    return response.json();
}

const data = await fetchApi('/users')

console.log(data.a)
```

[↑ top](#typescript-generic)
<br><br><br><br><hr>

### `type parameter constraints`

To make sure the calling code is always going to pass an object to your function

```typescript
function stringifyObjectKeyValues<T extends Record<string, any>>(obj: T) {
    return Object.keys(obj).reduce((acc, key) => ({
        ...acc,
        [key]: JSON.stringify(obj[key])
    }), {} as { [K in keyof T]: string })
}
```

[↑ top](#typescript-generic)
<br><br><br><br><hr>
