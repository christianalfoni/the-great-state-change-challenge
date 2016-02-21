# The Great State Change Challenge
A project to show diversity in solving real life complex application flows

### Background
We have built applications in the client using web technology for quite a while now. There is a huge number of challenges in our domain, but the open source community brings new tools almost every day. This can feel a bit exchausting from time to time. There are many great ideas, which looks really good in the popular "counter examples" and "todomvc examples", but these are not real life problems. You can create these two applications beauitfully and simply in any tool. We have to add more complexity to see the difference between our tools.

### The format of the challenge
There are three fundemental parts to building and application:

1. Define initial state
2. Define how to change the state
3. Define a UI to use state and trigger state changes

So this is our format and we are going to solve different scenarios in the spirit of "state driven applications"

### State driven applications
A state driven application is an application where the internal state of the application drives the UI. This is a very powerful concept that has been around for a long time, though has become a lot more clear with later implementations. The core idea is as an example is:

1. A state `{query: ''}` is defined in your application
2. The UI with an input subscribes to this state to display the current query
3. When input triggers a value of `f` it is synchronized with the internal state `{query: 'f'}`
4. The UI now reacts to this change and will put the new query value, `'f'` as the value of the input

**The two main benefits of this is:**
1. When some other part of your application wants to know the current query value it can do so by checking the internal state, not going into the DOM and check the input element
2. When some other part of your application wants to change the query value it can do so by changing the internal state, not going into the DOM and change the value there

#### Challenge example

##### The scenario
The application should have an input that will update the title state.

##### Given the following state...
```js
{
  title: ''
}
```

##### I want to change to the following state...
```js
{
  title: 'f'
}
```

##### Example solution
[Cerebral](cerebral/example)
