### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces. 

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.

```javascript
const whatToDoForLunch = function(hungry, availableTime) {
  let text = '';
  if (hungry === true) {
    if (availableTime < 20) {
      text = 'Pick something up and eat in back in the Lab or in the kitchen, where you can get to know your fellow classmates.';
    } else if (availableTime >= 20 && availableTime <= 30) {
      text = 'You deserve a break and could try a place in Gastown.';
    } else {
      text = 'This is a bootcamp after all and you should probably reconsider.';
    }
  } else {
    text = "Wait until you're hungry.";
  }
  return console.log(text);
};


/*
 * This is some test runner code that's simply calling our whatToDoForLunch function
 * defined above to verify we're making the right decisions. Do not modify it!
 */

console.log("I'm hungry and I have 20 minutes for lunch.");
whatToDoForLunch(true, 20);
console.log("---");

console.log("I'm hungry and I have 50 minutes for lunch.");
whatToDoForLunch(true, 50);
console.log("---");

console.log("I'm not hungry and I have 30 minutes for lunch.");
whatToDoForLunch(false, 30);
console.log("---");

console.log("I'm hungry and I have 15 minutes for lunch.");
whatToDoForLunch(true, 15);
```