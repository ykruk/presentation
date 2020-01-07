## presentation-Q3-2019 React JS

Hello! My name is Julia. 
I'm going to talk to you about today's really hot topic - React JS.


`(slide - What is React?)`

The first question we are going to cover - What is React?
React is technically a Javascript library created and maintained by Facebook and it is used for building web-interfaces and front-end applications. It was created by Jordan Walke, a Facebook employee in 2011 to minimize the time and effort spent in creating user interfaces for web apps and websites. In 2013 the project was open-sourced and is now being maintained by Facebook and individual developers and companies from all over the world.

`(slide - Is React a framework or a library?)`

The question of whether React is a library or a framework is one that keeps coming up. Although I already stated that it is, in fact, a library, I want to explain further why it is a library and not a framework.
One key difference between a framework and a library is that a framework defines the structure and architecture of your code. It dictates how your app is to be developed. You can think of it as a template.
A library is a collection of programs that perform common repetitive functions during development. This is precisely the way React is designed. It can be used to create UI components for your application or edit ones previously created with HTML. You define how you want to use it, which contrasts to how a framework functions.
So, React is *technically* a library, but still most people refer to it as a framework because of its behavior and capabilities.

`(slide - When is React used?)`

React was initially released by Facebook as a Javascript library for building user interfaces for the web. It has since advanced past that. In 2015, Facebook released React Native a cross-platform mobile framework which makes use of React to build user interfaces for Android and iOS.

`(slide - Does React need any additional setup?)`

Setting up React isn’t as simple as just launching a setup file. It involves a lot of processes. Asides installing the React library itself, there are other packages you need to install and a lot of configurations to make a complete React development environment.
You still have to install packages like webpack and babel and configure them to have a complete React development environment. You could probably skip installing these packages and develop simple projects without them, but for larger projects, you should have them installed.

`(slide - Can it be added to an existing project?)`

React being a library can be used with an existing project. After setting it up on your system, all you need to do is add the react and react-dom script tags to your existing HTML code, and then call the Javascript file containing the component you created with a script tag as well. Then you place a div tag with the components name as its id where you want the React component to be placed, and you’re good to go.

`(slide - How do I host React applications?)`

React applications can be hosted like any other web app. There are a lot of options you can choose from. You can host your React app on Github Pages, Netlify, Heroku and so many others although these are more suited for static websites. For dynamic sites, you might want to consider solutions like AWS, Microsoft Azure or Google Cloud.

`(slide - How performant is React?)`

React is quite fast, and it is so because of one main reason, the Virtual DOM. The DOM or document object model is a representation of your HTML code. It’s what gives Javascript the ability to manipulate HTML elements. It makes use of the DOM API to achieve this.
JavaScript allows us to manipulate with the DOM and create interactive web-interfaces. But with Vanilla JavaScript it's a lot more code, it's  much more difficult to do the same things that you could do with a framework. React makes it very easy to build front-end projects, it's also very organized and it uses self-contained independent components that have their own state and this allows to build really interactive user interfaces.
The React Virtual DOM is a simpler copy of the actual DOM which you interact with React. Instead of reloading the whole DOM each time there is a change in state, it re-creates the React DOM and compares it to the previous version using a difference algorithm. It then instructs the DOM to reload only the affected area. This significantly reduces the time taken to update a page.

`(slide - React Components)`

The central part of ReactJS paradigm is the concept of components.
Basically component is an isolated piece of interface, that can contain some layout, some bound state and some logic. Component can be as simple as just a button or text input, or it can be complex and be composed from many other simpler components.
Components can have children components inside of them, that can have their children and so on.
This allows you to describe your application UI as a nested tree of components (which we can see on the second picture).

`(slide - Creating a React Component)`

There are two major ways of defining components: using functions and using classes.
When defining a component as a class you extend React.Component. Like this:
    class SimpleComponent extends React.Component {
			render() {
			return <div>Very basic component.</div>;
      }
		}
If you define your component using class - you should define render() method.

`(slide - Composing Components)`

Biggest strength of using components is that you can break down complex UI into small and manageable pieces.
Inside your components you can refer to other components and render them as children. As in the example:

		const Header = () => <>{/* Some Header Layout */}</>;

		const LoginForm = () => <>{/* Login Form Layout */}</>;

		const LoginPanel = () => (
			<div>
				<LoginForm />
			</div>
		);

		const LoginPage = () => (
			<>
				<Header />
				<LoginPanel />
			</>
		);

`(slide - Rendering Your Components)`

Typical React application has one root component that is being rendered to DOM. Inside that component it refers to all other components that belong to the app.

		const App => () (
			<h1>Simple app.</h1>;
		)

		ReactDOM.render(
			<App />,
			document.getElementById('root')
		);

Here we call ReactDOM.render() with the `<App />` element. Our App component returns a `<h1>Simple app.</h1>` element as the result. ReactDOM updates the DOM to match `<h1>Simple app.</h1>`.

As we have seen so far, React components are fairly simple. They can have internal `state`. They can also accept `props`. Beyond this React provides escape hatches that allow you to handle advanced use cases. These include lifecycle methods and `refs`. There are also a set of custom properties and methods.

`(slide - Lifecycle Methods)`

From the image on the slide we can see that a React component has three phases during its lifecycle. It can be mounting, mounted, and unmounting. Each of these phases comes with related methods.
We are not going to get deeper for now.

`(slide - Props)`

Short for properties, props can best be defined as a way of passing data from component to component, basically from parent to child component.

		class BasicProp extends React.Component {
			render() {
				return <h1>Hello {this.props.name}</h1>;
			}
		}
		
		React.render(<BasicProp name="Jake" />, document.getElementById('app'));

`(slide - What are the advantages of React?)`

Now when we've quickly run through React basic features, lets recap. 
What are the advantages of React?
- The use of a virtual DOM makes React apps faster.
- With React you can re-use previously composed components.
- There is support for server-side rendering of websites.
- You do not need to worry about framework-specific code as React is a library.
- React also makes it easy to work with teams because it's organized and everyone can be on the same page. You can assign different developers to work on different components rather than just having one big code sheet that is very confusing for multiple people to work on.

`(slide - What are the cons of React?)`

React just like a lot of things has disadvantages. Some of them are:
- React is continuously and frequently being improved. It might be hard to follow the pace of development.
- JSX or Javascript extension, which is used in creating React components, can be quite hard to learn.
- Unlike with frameworks that define how your app is to be structured, you have to structure your app yourself. This is not necessarily a disadvantage if you know how to.

Now we've gone through a quick review of React. And thank you all for watching.