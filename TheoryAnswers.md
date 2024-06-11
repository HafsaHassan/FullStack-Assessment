
## Question 1
Design Heuristics consist of 10 Usability Heuristics, pioneered by Jakob Nielsen, which were created as a guide for developers to refer to for design choices. Each Heuristic provides speicifc needs which need to be met in order to provide best practices and usability for the end user.

"Matching Between System and Real World", also known as H2, is the second Heuristic in Neilsen's framework. This Heuristic advises developers that their design should contain familiarity for their users. This would include concepts, wording/terms, images and logic that the user is already accustomed to. The reason for this Heuristic is to create natural mapping - minimising the amount a user needs to rely on their memory and understanding to use the system or preform tasks. Therefore, by following real world conventions, the design will make it easer for users to get to the desired outcomes as the system will be simpler for them to use and they will retain the information on how the interface works.

An example of H2 not being met, therefore causing a usability problem, would be a university application for students having a library card available on the app but not a student ID card. 
The reason for this violation would be since, in the real world, students would use their student ID card as their library card, therefore, would not have the need to carry both but in the application there is a distinct difference between the two cards and this creates inconsistancy with their real world experience, as the card on the app would only be used for the library and not for all Student ID purposes. Therefore, if the app did not have a digital version of their Student ID, they would still need to carry the physical copy, and this does not align with the real world use case and creates confusion.

Advantages of adhereing to this heuristic would be:

Higher user satisfcation - Users will be less frustrated with the system if they can use the it without intervention and learning new concepts. They will run into less errors and be able to complete tasks and get their desired outcome on their own, based on concepts they are already used to.

Increased accessability - More people would be able to use the system, if it mimics real world concepts and familiarity, because less technical knowledge and logic would be required, therefore, anyone of any level of understanding and those with cognitive disabilities can easily use the system.

Quicker onboarding - Reduced training will be required for users and it will be simpler to introduce to new users since the concepts are already known and a huge learning curve will be avoided.

Overall, design heuistics are important to adhere to for an imporved user experience. In regards to heuristic Matching Between System and Real World, many advantages are linked by implementing this due to familiarity of previous concepts.

## Quesion 2
The Single Source of Truth (SSOT) is a concept which requires data to be placed in only one location, in order to maintian this information easily in the future from just one storage space. Reason for this is to eliminate data redundancy - where data is kept in more than once place and can cause conflicts within the system. Conflicts would arise because if all pieces of data were not updated, this would cause inconsistencies and discrepancies in the system. By having only one area where the data is located, it only needs to be updated once.

In regards to Redux - a state management library used in React - SSOT is implemented by nature. This is done by a central store which contains the full state of the system and this state is immutable - meaning the state itself cannot be changed and if changes are required then reducers are used to describe the new changes, creating a new state. Therefore, Redux is the SSOT for React applications as it holds the entire state of the system and this can only be modified through the central store, ensuring data is only stored in one location.

An example of this would be by creating a Redux store - to manage the state, having a reducer  - to change the state in regards to speicifc actions and having components - which connect the React components to the store. Below are example coding snippets of a store and reducer for increasing and decreasing values to then update the state:

Store.js:

```js 
const Store = createStore(reducerCounter);

```

Reducer.js: 

```js
const initialState = {
    count: 0
}

const reducerCounter = (state = initialState, action) => {
    if (action.type === increase) {
        return {count: state.count + 1}
    } else if (action.type === decrease) {
        return {count: state.count - 1}
    } else {
        return state;
    }
}
```

Advantages of SSOT would be:

Consistancy: Since the data is only stored in one place, there will be no duplicate entries to maintain, which would also reduce version control problems. Redux also implements a one way directional pattern, therefore, there will only be one process to add/change/remove the data from the state.

Simplified debugging: Since a central store is used, the system's state is kept in this one location which makes it easier to maintain and find for any issues related to state management, since there is only one place to go for this.

Simplified Testing: Redux allows for reducers and actions to be tested separately from UI components, therefore, speicifc tests can be focused on only logic without having to also test UI components. Also in Redux, since reducers follow a one directional approach, they give the same output for the same input and won't alter outside of this, making testing simplified by making sure the reducer generates the new state.

Overall, having a SSOT like Redux poses many benefits which makes it easier to maintain data and reduce time taken to fix issues, since there is only one location to look for.

## Question 3



## Question 4



