# Javascript: Design Pattern

- [`module pattern`](#module-pattern)
- [`revealing module pattern`](#revealing-module-pattern)

[↑ top](#javascript-design-pattern)
<br><br><br><br><hr>

### `module pattern`

<br>

> In JavaScript, the Module pattern is used to further emulate the concept of classes in such a way that we’re able to
> include both public/private methods

<br>

```javascript
var personModule = (function () {

    var firstName;
    var lastName;

    return {
        setName(f, l) {
            firstName = f;
            lastName = l;
        },
        getName() {
            return firstName + " " + lastName;
        }
    }

})();

personModule.setName('akash', 'pal')
personModule.getName() //"akash pal"

```

<br>

[↑ top](#javascript-design-pattern)
<br><br><br><br><hr>

### `revealing module pattern`

<br>

```javascript

var personModule = (function(){
  
  var firstName;
  var lastName;
  
  function setName(f,l){
    firstName = f;
    lastName = l;
  }
  
  function getName(){
    return firstName + " " + lastName;
  }
  
  return{
    setName:setName,
    getName:getName
  }
  
})();

personModule.setName('akash','pal');
personModule.getName(); //"akash pal"

```

<br>

[↑ top](#javascript-design-pattern)
<br><br><br><br><hr>
