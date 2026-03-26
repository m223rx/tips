# ⚡ JavaScript Tip #010 — Optional Chaining

Avoid errors accessing nested properties.

```javascript id="js-optional"
const user = {profile: {name: "Mohamed"}};
console.log(user.profile?.name);    // Mohamed
console.log(user.address?.city);    // undefined
```
