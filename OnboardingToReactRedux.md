# Onboarding to React and Redux
*!DISCLAIMER: THIS IS NOT A TEST. IT IS JUST A STEP BY STEP PROCEDURE TO UNDERSTAND AND GET USED TO REACT AND REDUX*


## Step 1: 
Read through the basics of React and understand the basic underlying concepts (A good starting point would be the React tutorial [here](https://reactjs.org/tutorial/tutorial.html)). You should be able to answer questions like the following:
- What is a React Component? What is the benefit of creating and using components?
- How can you compose a React Component?
- What are Props and State. How are they different from one another? What they are used for?
- What are functional components?
- What is the Component lifecycle? How is it used? What are its advantages? When and why should one override these methods?
- What is a template language (like JSX) and why is it useful to write UI components with such a DSL (domain specific language)
- What is JSX, what is JSX translated to after transpiling?
- Composition over inheritance. Explain the concept, benefits.
- What is the reconciliation process? How does the application gets updated/ re-rendered?
- What is immutability? Why is it important?
- What are Controlled and Uncontrolled input components? Example scenarios where they can be used.


## Step 2:
Here begins the fun part - Hands On!

### Scenario:
I am a big company and you are a freelancer. I outsource certain smaller tasks that I do not want to do.

#### Day 1:
I want a component generates(just generate. Not send.) a welcome email for Mr. John Doe. Body of the email not important(Lorem ipsum will do). Use of any HTML tag would be fine.

#### Day 2:
Now, I am the client, so I am allowed to change my mind. :P

What will I do with a component that is just for Mr. John Doe? I do not want to have millions of components for just an email (Yes, millions of customers, Big company, remember?).

Now, I want a component that accepts first name and last name and generates a welcome email for that specific person.

#### Day 3:
Good job! But, now I think it will be more useful to have an input field that accepts the name and the email is generated for the name entered in the input field.

#### Day 4:
Did you insert the input field in the same component?
If no, you need not do this step.
If yes, I would want to have the logic to just generate the email separate, so that I can reuse it. Because a component with an input field and an email template is not reusable. (Hint: Composition)

#### Day 5:
Now, I need some more functionality in the Components. The Component which initially accepted only name should now be a form that accepts the name, email address and date of birth. And the Component which generated the email should include the first name, the email address and age based content for the user. So, different contents for users with age < 30, >30 and >60.

#### Day 6:
Good job! Now create a list to save the details of the user that I am adding (temporary is fine). The list of these contacts is displayed on the same page.

#### Day 7:
Now when I click on one of the contacts from the list, an email for that specific user should be generated with his first name, the email address and age based content for the user.
(State Management comes into the picture).

Now that we have a basic idea of how to use React in our day-to-day applications, we would extend our learning to Redux. To get used to how Redux works, it is helpful to watch and learn from Dan Abramov the co-author of Redux [here](https://egghead.io/courses/getting-started-with-redux)

Using the knowledge that we just acquired, we can start converting the state that we used in our application and convert it to Redux State.
The major difference that we see here is that, when we use React State, if the top-most component needs access to any mutable variable, it is added to the state of that component and all the children components that need to access that variable are provided with that variable via Props. Whereas, in Redux state, the state is stored globally in a Redux store and any of the Components irrespective of their hierarchy can access the variable without explicitly passing that variable as a Prop.
Once the conversion from React State to Redux State is done, you should be able to answer the following questions:
- What are Containers?
- What is the use of mapStateToProps and mapDispatchToProps
- What are the two ways of creating Redux Action?
- What is a reducer?
- What is immutability? Why is it important?
- What are the advantages of using Redux?

To not have any misconceptions about Redux, it is recommended to read the following article: [You Might Not Need Redux](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367) by Dan Abramov (Yes, you read that right).

After having read the above article, there is an open question that needs to be answered (And it does not have one correct answer):

Did we need to use Redux in the project that we created?
