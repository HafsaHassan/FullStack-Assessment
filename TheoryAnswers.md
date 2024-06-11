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

An example of this would be by creating a Redux store - to manage the state, having a reducer - to change the state in regards to speicifc actions and having components - which connect the React components to the store. Below are example coding snippets of a store and reducer for increasing and decreasing values to then update the state:

Store.js:

```js
const Store = createStore(reducerCounter);
```

Reducer.js:

```js
const initialState = {
  count: 0,
};

const reducerCounter = (state = initialState, action) => {
  if (action.type === increase) {
    return { count: state.count + 1 };
  } else if (action.type === decrease) {
    return { count: state.count - 1 };
  } else {
    return state;
  }
};
```
Advantages of SSOT would be:

Consistancy: Since the data is only stored in one place, there will be no duplicate entries to maintain, which would also reduce version control problems. Redux also implements a one way directional pattern, therefore, there will only be one process to add/change/remove the data from the state.

Simplified debugging: Since a central store is used, the system's state is kept in this one location which makes it easier to maintain and find for any issues related to state management, since there is only one place to go for this.

Simplified Testing: Redux allows for reducers and actions to be tested separately from UI components, therefore, speicifc tests can be focused on only logic without having to also test UI components. Also in Redux, since reducers follow a one directional approach, they give the same output for the same input and won't alter outside of this, making testing simplified by making sure the reducer generates the new state.

Overall, having a SSOT like Redux poses many benefits which makes it easier to maintain data and reduce time taken to fix issues, since there is only one location to look for.

## Question 3
Stateful components, in React, hold infomration and data about their components. The component state can be altered, through re-rendering. When the attrubutes of a state are changed, the component is also changed. Stateful components hold their own state through "this.state" or "useState" components, for example. Content can be rendered, based on the state, so if changes are made the components will re-reder and show the new state.

Stateless components

Unlike stateful components, stateless ones do not manage their own state and instead rely on props passed from their parent componenents, therefore they have no state management. Stateless components are important for UI elements and optimising performance.

Differences:

- Stateful componenets are usually more complex due to data handeling and logic compared to stateless componenents.

- Stateless components are simple and more focused on UI through props and rendering static content.

- The re-rendering aspect of stateful components can cause them to be less efficient, when not managed correctly, compared to stateless ones.

However, it is worth mentioning since the introduction of React Hooks, the gap between stateless and stateful components has been bridged since the Hooks allow for funcational components, normally stateless, to also manage state.

Below is an example code snippet of a stateful component and stateless component:

Stateful.js

```js
const Counter = () => {
  const [count, setCount] = useState(0);

  const inreaseCount = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p> Count: {count}</p>
      <button> onClick = {increaseCount}>Increase</button>
    </div>
  );
};
```

Stateless.js

```js
const Greeting = (props) => {
  return <p> Hello, {props.name} </p>;
};
```

## Question 4
Scripted testing is an approach in which testers will follow set steps, in their testing. Testers will stick to their given steps and will not do anything outisde of this. Although, testers can automate their test cases or write them manually. Scripted testing would best be used in scenarios of high risk, such as software used for finanical reasons. This type of testing does require extensive planning and documentation - due to detailed test cases, therefore, it is time consuming.

Exploratory testing is another testing approach, however, in this approach testers do not have pre-defined scripts to follow and instead rely on their knowledge and experiences to find defects. This test approach does require more creativity and testers can alter their tests throughout the process as they learn more about the system/application over time. An example of when this testing would be used is on a mobile application, to identify usability issues on different devices and operating systems. Testers can adapt to the application's behaviour to discover defects.

Advantages of Scripted Testing:

- **Detailed documentation.** Since extensive documentation is done, testers will be able to refer back to this and test cases can be reused and reviewed later.
- **Compliance.** For strict environments, adhering to scripted tests will make sure companies are compliant with regulation and policies.
- **Suitable for regression testing.** Test cases can be repeated in the same manner.

Disadvantages of Scripted Testing:

- **Time consuming.** Significant planning, documenting and maintaining is required.
- **Reduced Flexability.** Cannot alter the tests if unexpected outcomes arise or changes happen.
- **Reduced time for testing.** Testing cannot start until the scripts are written which can delay the testing period.

Advantages of Exploratory Testing:

- **Flexability.** Testers do not have pre-defined scripts to follow and can create new tests based on the information discovered.
- **Find unexpected bugs.** Since exploratory testing encourages creativity, testers can work away from a script and test based on their new findings, which would allow them to discover and fix unexpetced issues and bugs, which scripted tests might not discover.
- **Quick to start.** Requires less preperation so testing can start quickly and keep happening throughout the development process.

Disadvantages of Exploratory Testing:

- **Reduced documentation.** Formal documenation is not emphaisesed, therefore, tracking tests can be more difficult and critial issues can be missed out.
- **Inconsistancies.** Test coverage of the system/application might not be complete or could vary based on the tester's approach and experience. Tester's may also have bias which can impact the outcome.
- **Need skilled testers.** Since this type of testing is based on tester skills and experience, unexperienced testers may not do thorough testing and may miss important details.
