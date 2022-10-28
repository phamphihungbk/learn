# PHP: String

- [`string interpolation`](#string-interpolation)

[↑ top](#php-string)
<br><br><br><br><hr>

### `string interpolation`

<br>

**without printf**

```php
$variable = "World";
$output = `Hello ${variable}!`;
echo $output

# Hello World

```

<br>

**using printf**

```php
$variable = "World";
$template = "Hello %s!";
$output = printf(template, $variable);
echo $output

# Hello World

```

<br>

[↑ top](#php-string)
<br><br><br><br><hr>
