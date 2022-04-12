## **Different phases of React LifeCycle**

---

There are three different phases of React component's lifecycle:

* **Mounting Phase:** When an instance of a component is being created & inserted into the DOM.

1. ***constructor( ):*** It is special type of function that will get called whenever a new component is
   created and is used to initialize the states & binding the event handlers. Never perform HTTP requests.

   ***super( ):*** It is used to call the constructor of its parent-class in-order to access the properties & methods
   of its parent-class.
2. ***static getDerivedStateFromProps( )***: When the state of component depends on change in props or
   setting up the state. Never perform HTTP requests. (rarely used)
3. ***render( ):*** Mandatory method and it returns the JSX, also children-component lifecycle methods also get executed.
   Never perform HTTP requests.
4. ***componentDidMount( ):*** Invoked immediately after a component and its child components have been successfully rendered to the DOM. Performs any AJAX call / HTTP requests to load data.

* **Updating phase:** When a component is being re-rendered based on change in
  state or props.

1. ***static getDerivedStateFromProps( ):*** Method is called every time a component is re-rendered. Inside, we can set the state & most important never perform any HTTP request.
2. ***shouldComponentUpdate( ):*** Dictates if the component should re-render or not & helps to optimize it's performance most important never perform any HTTP request.
3. ***render( ):*** Mandatory method and it returns the JSX. Never perform HTTP requests.
4. ***getSnapshotBeforeUpdate( ):*** Called right before the changes from the virtual DOM are to be reflected in the DOM. (rarely used)
5. ***componentDidUpdate( ):*** Called after the render is finished in the re-render cycles.

* **Unmounting Phase:** When a component is being removed from the DOM.

1. ***componentWillUnmount( ):*** Method is invoked immediately before a component is umounted and destroyed.  Cancelling any network required.
