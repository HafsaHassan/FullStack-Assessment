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

# Question 3

## Section 2 Coding



## Section 3 Theory

# Question 1

# Question 2

# Question 3

# Question 4

