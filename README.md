# ES6note
My note for studying Javascript ES6

### Import and Export
#### Basic Import
To import a module into a script:
```javascript
import React from 'react'
```
This will import the default export by the react package.
#### Basic Export
To export a class
```javascript
class App {
    constructor(name) {
        this.name = name;
    }
}

export default App;
```
#### Export vs. Export default
If you use export default, you use any name when importing the module. For example,
```javascript
import myApp from './App';
```
But when you use export without default, you have to specific the exact names of what you want to import in a pair of curly braces. For example,
```javascript
class App {
    constructor(name) {
        this.name = name;
    }
}

export default App;
export const height = 80;
export const weight = 60;
```
In another file, do

```javascript
import myApp, {height, weight as myWeight} from './App';
```
Note that you can still use a name alias.
