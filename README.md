<h1 align="center">Welcome to fast-db 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-1.0.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/Aleks-1123/fast-db#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/Aleks-1123/fast-db/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/Aleks-1123/fast-db/blob/master/LICENSE" target="_blank">
    <img alt="License: ISC" src="https://img.shields.io/github/license/Aleks-1123/fast-db" />
  </a>
</p>

> A small SQLite wrapper

### 🏠 [Homepage](https://github.com/Aleks-1123/fast-db#readme)

## Install

```sh
npm install fast-db --save
```

## Using

```js
let Database = require("fast-db");

let db = new Database({
    path: "./db.sqlite", // path to database file (optional, default ./database.sqlite)
    table: "testing" // default table (optional, default master)
});

/* Basic usage */
let foo = db.get("foo");
console.log(foo) // null
let operation = db.set("foo", "bar");
console.log(operation) // true
let newFoo = db.get("foo");
console.log(newFoo) // bar

/* Using tables */

db.table("foo");


let operation = db.set("foo", "bar");
console.log(operation) // true
let newFoo = db.get("foo");
console.log(newFoo) // bar

let newFooFromOtherTable = db.table('bar').get('foo');
console.log(newFooFromOtherTable); // null !
```

## Author

👤 **Aleks1123**

* Website: http://aleks.ovh
* Github: [@Aleks-1123](https://github.com/Aleks-1123)

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2021 [Aleks1123](https://github.com/Aleks-1123).<br />
This project is [ISC](https://github.com/Aleks-1123/fast-db/blob/master/LICENSE) licensed.

***