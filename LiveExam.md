## Section 1 Redux

# Question 1

1. The reducer (countReader) is responsible for showing the changes to the state when the changes are doen through actions and sent to the store. The function is checking if action.type is increment, if it is then a new state will be shown and the value will be increased by 1. If three is no increment then the current state will be shown.

2. Similar to the increment action, a decrement action can be added and if it is found then the state.value will decrease by 1 and this new state will be returned. Example:
```js
else if (action.type == 'decrement') {
    return {
        value: state.value -1
    }
}
```

3. A reset action.type would need to be added and this would need to return the state to its original value which is initialState. Example:
``` js

else if (action.type === 'reset') {
    return initalState;
}
```

# Question 2

1. The state is being initialised with studentsCount and is being set to the value 0, the setStudentCount will update the state. The number of students in a class is being returned/displayed, from the state - studentsCount. Next there is a button that adds a student when it is clicked but the function is missing.

2. 
    First the students data would be put into an array. 
    Then a function would be created to count the number of students. 
    A counter would be added starting at 0, then the student data array would need to be looped through to check if the student is present (value would need to be true). 
    An if statement would be used for this and if true then the counter would increase. 
    Then the counter would be returned. 
    A new function would need to be made to update the student count, the function which was counting the number of students would be called to get the number of present students.
    Then the state would be updated with a function to set the students count with the value from the function counting the present students.
    Lastly, the onClick button would be updated with an event handler to call on the updated student count function.

# Question 3

1. The payload was added and by doing this the state's value will change with the payload in the action. If the increment action in line 170 is true then the payload will increment its value by 1.

2. To do this, the reducer and inital state would need to be set up in our component and would need to dispatch an action with the right payload when the button is clicked.

3.  The best suited solution is figure 2 because the increment action updates the state with the correct number of students that are present as it sets the exact number of students present every time the button is clicked. Whereas, figure 1 could give incorrect values when the increment is used lots of different times without considering the values from the beginning.


## Section 2 Coding

```js
function isPalindromeTrue(str) {
    let reversedStr = "";

    for (let i = str.length - 1;
        i >= 0;
        i--) {
            reversedStr += str[i];
        }

        if (str === reversedStr) {
            return true;
        } else {
            return false;
    }
}

console.log(isPalindromeTrue("radar")); // true
console.log(isPalindromeTrue("level")); //true
console.log(isPalindromeTrue("pencil")); // false
console.log(isPalindromeTrue("a")); // true
```

## Section 3 Theory

# Question 1

# Question 2

# Question 3

# Question 4

