A variable can be assigned only at one place.

```js
//bad
let name = 'Joe';
let nickname;
if (!name) {
  nickname = defaultNickname;
} else if (typeof nicknames !== 'undefined' && nicknames[name]) {
  nickname = nicknames[name];
} else {
  nickname = name;
}

//good
function getNickname(name) {
  if (!name) {
    return defaultNickname;
  }
  if (typeof nicknames !== 'undefined' && nicknames[name]) {
    return nicknames[name];
  }
  return name;
}

let name = 'Joe';
let nickname = getNickname(name);
```
