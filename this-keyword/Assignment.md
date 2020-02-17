### Assessment Quiz

Answer with proper reasoning. Write down your thoughts step by step
and answer the question:

Question #1

```js
function logThis() {
  console.log(this);
}

const myObj = {
  logThis
};

myObj.logThis();
```

Question #2

```js
function logThis() {
  console.log(this);
}

const myObj = {
  foo: function() {
    logThis();
  }
};

myObj.foo();
```

Question #3

```js
const logThis = () => {
  console.log(this);
};

const myObj = {
  foo: logThis
};

myObj.foo();
```

Question #4

```js
function logThis() {
  console.log(this);
}

const myObj = { name: 'sag1v' };

logThis.apply(myObj);
```

Question #5

```js
const logThis = () => {
  console.log(this);
};

const myObj = { name: 'sag1v' };

logThis.apply(myObj);
```

Question #6

```js
function logThis() {
  console.log(this);
}

const someObj = new logThis();
```

Question #7

```js
function logThis() {
  'use strict';
  console.log(this);
}

function myFunc() {
  logThis();
}

const someObj = new myFunc();
```

Question #8

```js
function logThis() {
  console.log(this);
}

class myClass {
  logThat() {
    logThis();
  }
}

const myClassInstance = new myClass();
myClassInstance.logThat();
```

Question #9

```js
function logThis() {
  console.log(this);
}

class myClass {
  logThat() {
    logThis.call(this);
  }
}

const myClassInstance = new myClass();
myClassInstance.logThat();
```

Question #10

```js
class myClass {
  logThis = () => {
    console.log(this);
  };
}

const myObj = { name: 'sagiv' };

const myClassInstance = new myClass();
myClassInstance.logThis.call(myObj);
```

Question #11

```js
const call = {
  caller: 'mom',
  says: function() {
    console.log(`Hey, ${this.caller} just called.`);
  }
};

call.says();
```

Question #12.

```js
const call = {
  caller: 'mom',
  says: () => {
    console.log(`Hey, ${this.caller} just called.`);
  }
};

call.says();
```

Question #13.

```js
const call = {
  caller: 'mom',
  says: function() {
    console.log(`Hey, ${this.caller} just called.`);
  }
};

let newCall = call.says;

newCall();
```

Question #14.

```js
function anotherCaller() {
  console.log(`${this.caller} called, too!`);
}

const call = {
  caller: 'mom',
  anotherCaller: anotherCaller,
  says: function() {
    console.log(`Hey, ${this.caller} just called.`);
  }
};

let newCall = call.anotherCaller;

newCall();
```

Bonus Questions:

Question #15

```js
function logThis() {
  console.log(this);
}

const btn = document.getElementById('btn');
btn.addEventListener('click', logThis);
```

Question #16.

```js
const logThis = () => {
  console.log(this);
};

const btn = document.getElementById('btn');
btn.addEventListener('click', logThis);
```
