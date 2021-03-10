## Redux is more useful when:

- You have large amounts of application state that are needed in many places in the app
- The app state is updated frequently over time
- The logic to update that state may be complex
- The app has a medium or large-sized codebase, and might be worked on by many people

**Not all apps need Redux. Take some time to think about the kind of app you're building, and decide what tools would be best to help solve the problems you're working on.**

## Immutability: Redux expects that all state updates are done immutably.

**In order to update values immutably, your code must make copies of existing objects/arrays, and then modify the copies.**

We can do this by hand using JavaScript's array / object spread operators, as well as array methods that return new copies of the array instead of mutating the original array.


## Redux terms

- Action:
```javascript
const addTodoAction = {
    type: 'allTodoAction/add',
    payload: {
        name: '',
        time: '2021-01-12'
    }
}
```

- Action Creators:

```javascript
const addTodoActionCreator = ( payload ) => {
    return { ...addTodoAction, payload };
}
```
- Reducers:

```javascript
(state, action) => newState

const initialState = {
    todos: []
}

const todoReducer = (state = initialState, action) => {
    if(action.type === 'allTodoAction/add') {
        return {
            ...state,
            {
                todos: [
                    ...state.todos,
                    action.payload
                ]
            }
        }
    }
}
```

- Selectors

Selectors are functions that know how to extract specific pieces of information from a store state value. As an application grows bigger, this can help avoid repeating logic as different parts of the app need to read the same data:

```javascript
const selectorCount = state => state.count.value
const currentCount = selectorCount(store.getState())
console.log(currentValue)
```

## DataFlow

![](./ReduxDataFlowDiagram.gif)