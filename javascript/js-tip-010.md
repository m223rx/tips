# ⚡ JavaScript Tip #010 — Optional Chaining

Avoid errors accessing nested properties.

```javascript id="js-optional"
const user = {profile: {name: "m223rx"}};
console.log(user.profile?.name);    // m223rx
console.log(user.address?.city);    // undefined
```
