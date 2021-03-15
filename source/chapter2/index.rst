React Components
================

* Finally we are ready to start coding in React and we'll start off with the basics of components.
* React components are reusable pieces of code that function independently, but can be used in conjunction with other
  components. They act as JavaScript functions and return HTML in the browser.
* This is done through the use of JSX (JavaScript XML).
* As previously stated components in React can either be functional or class based.
* Class based components require us to extend the React Component class, and also require a render method to return HTML.
* This gives access to React.Component's built in functions.
* In class based components it is common to see the use of a constructor method to initialize state, but it isn't
  necessary as state can be initialized without it.
* Functional components require none of the requirements mentioned above, but have some other requirements instead such
  as the use of React hooks.
* When creating a component in React the name of the component needs to start with an uppercase letter.
* An example of class based components will be shown in this tutorial, but functional components will be preferred.



Class Based Component Set Up
----------------------------

* First we'll create a folder for our class based component and call it ClassComponent.
* In order to do this you'll need to left click on the src folder and locate the new folder icon in the drop down.
* Select new folder and name this folder ClassComponent.

    .. image:: create-folder.*

* Inside this folder we'll create a file called ClassComponent.js. To do this left click the folder and locate add file
  in the drop down.

    .. image:: add-file.*

* After you've created the folder and file open the ClassComponent.js file. This is where the code from the next
  section will be added.

Class Based Component Implementation
------------------------------------

* In order to use class based components one must first use the following syntax in order to import the component class
  from React, so add this to the top of the file.

.. code-block:: javascript
    :caption: Importing Component

    import React, { Component } from 'react'


* Once that is done we can build a class based component, and it begins to look like the code below.
* It's important that the export statement isn't forgotten as this allows for components to be imported to other
  components and ultimately the final app component.
* As you can see here we're defining our component as a class, giving the components a name, and extending the Component
  class that we imported.
* This import is necessary because all React class based components are children of the React Component class.

.. code-block:: javascript
    :caption: Class Based Component

    import React, { Component } from 'react'

    class ClassComponent extends Component {
        render() {
            return (
                <div>

                </div>
            )
        }
    }

    export default ClassComponent;

* The return statement inside of the component is where JSX (JavaScript XML) can be used to describe what the UI should
  look like, and it closely resembles HTML.
* It is written mostly like HTML but one of the more immediately identifiable differences is the fact that className
  is used to describe a class in JSX instead of class (which is what we would use in HTML5).
* This is the way that all HTML element attributes are written in JSX because JSX requires camel case for HTML attributes
  and CSS selectors as well.
* Go ahead and enter this code inside of the div in the return statement.

.. code-block:: javascript
    :caption: Example of JSX
    :linenos:
    :emphasize-lines: 6,7,8,9,10,11

    import React, { Component } from 'react'

    class ClassComponent extends Component {
        render() {
            return (
                <div>
                    <header className="header">
                        <h1>Hello World</h1>
                    </header>
                </div>
            )
        }
    }

    export default ClassComponent;


* In order to render this component you need to import it to your app component. so that it is exported to the
  index.html document for rendering.
* In order to do this open the App.js file and add the highlighted code to the file.

.. code-block:: javascript
    :caption: Nesting Class Component In App Component
    :linenos:
    :emphasize-lines: 2,7

    import React, { Component } from 'react'
    import ClassComponent from './ClassComponent/ClassComponent'

    class App extends Component {
        render() {
                return (
                    <ClassComponent/>
                )
            }
        }

    export default App;

* This would in turn allow your component to be rendered in the index.html document inside of the div with an id of "root".

.. literalinclude:: index.html

* After this step run npm or refresh the browser and it should look like the image below.

    .. image:: hello-world.*

Introduction To Props
---------------------
* Props or properties are how we transfer data down to child components.
* We can use props to pass many things down in React such as functions, variables, and array objects just to name a few.
* Here we will create a variable that holds a string and pass it down as a prop from the App component to the
  ClassComponent.

    .. image:: prop-variable.*

* Once this is done we can pass the variable as a prop into the ClassComponent with the following underlined syntax.

    .. image:: passing-prop.*

* We essentially name the prop and set it equal to its JSX value inside curly braces.
* After this we can head back over to the ClassComponent.js file and insert an h2 tag with the following code under the
  h1.
* This will successfully pass our variable as props down from the App component to the ClassComponent.

    .. image:: render-prop.*

* Now we can refresh the browser window and you should now see the Hello World string that we passed as props to the h2
  in ClassComponent.

    .. image:: hello-world-h2.*

* We can also pass CSS styles as props.
* Here we'll create a variable called TextStyle and our value will be some CSS styling as shown below.
* From here we'll pass it to our ClassComponent just as we passed the string variable.

    .. image:: css-props.*

* After you've done this add the TextStyle to the h2 in ClassComponent.js.

    .. image:: ClassComponent-css-props.*

* Now you should see the following in the browser window.

    .. image:: hello-world-color-change.*

Introduction To State
---------------------
* State is an object in React, and it is used to store component values that belong to a particular component.
* State is mostly used for values that change based upon certain conditions whereas props are static and unchanging.
  and this is the main difference between state and props in React.
* State can be passed down as props if state values for a particular component need to be used in several components.
* Here we will create a piece of state to hold the color value of the ClassComponent as opposed to passing it as a prop
  from the App component, so make sure that you return to the App component and remove the code that we used to pass
  down the styles.
* The app component should now look as it is depicted below.

    .. image:: passing-prop.*

* Now we can create our piece of state in ClassComponent.js and pass it into the h2 element.

    .. image:: class-state.*

* This will have the same effect as what we've done previously, but now we can use this state to apply some logic to how
  the values will behave.
* From here we'll add a button below the h2 element in the ClassComponent.

    .. image:: class-state-button.*

* Now we can create a function to change the value of the state component, and consequently change the colors of the h2
  component.
* First we'll have to add a count property to our state object.
* Then we implement our function and pass it into the button element in the return method of our class function.
* Notice how we named the property in the button onClick. This is necessary because onClick is a built in function that
  allows our function to work upon clicking the button.
* Also notice that it is necessary to wrap the CSS in curly braces in order for it to function.
* This is because the CSS styles we're implementing are being interpreted as JavaScript.
* Take note of the use of this in the syntax as well. In this case this refers to the state object and it allows us to interact
  with the state objects values.
* setState used in the colorChange arrow function is a built in function that we can use to change state values.

    .. image:: class-state-colorChange.*

* After the previous steps are properly implemented you should be able to refresh the browser and clicking the button
  should alternate between the different state values defined in the function.

    .. image:: color-change.*

* We could also show the count in the HTML by adding it into a new h3 element tag and using the syntax this.state.count
  in curly braces inside of the h3.
* This will give us a value of zero shown on the screen, but as we click the color change button, we can watch the number
  go up as the colorChange function increases its value.
* Notice here that a new function has been added called decrement.
* This function gives you the ability to count up and down, but notice that it doesn't affect the CSS styles of the h2
  element.
* This is because the decrement function is operating independently of the colorChange function and is not tied into its
  logic.

    .. image:: count-code.*

* After the following steps refreshing your browser show the following below.

    .. image:: counter.*


Functional Components
---------------------

* React functional components do not require any import statements at first in their basic form. They are simply defined
  as JavaScript arrow functions and take props as a parameter.
* Adding props as a parameter is necessary in order to pass props down to functional components.
* Here you should follow the same steps that were required to add a folder and file for the ClassComponent except we're
  going to call this new folder FunctionalComponent, and we'll call the file FunctionalComponent.js.
* Here you should see a blank document, but we're going to quickly add a boilerplate for our functional component by
  typing the shortcut "rafce" into the blank document and hitting enter.
* This looks like the following below.

    .. image:: functional-component.*

* Once you hit enter it should show an arrow function with the corresponding name of our .js file as the name of our
  function and an export statement should also be included.

    .. image:: functional-component-boilerplate.*

* This boilerplate includes an import statement, but we do not need to import React here so it can stay or go.
* First we want to make sure that props is passed in as a parameter like so.

    .. image:: functional-component-props.*

* Here we'll return to App.js and do the same exact thing as before, but this time we'll be using a functional component.
* This will require the useState Hook, so we will have to import that.
* We'll also be passing down our state and functions as props here so we can see what that looks like here.
* First we'll comment out the ClassComponent that's nested in the return statement of the App function, and the import
  ClassComponent statement at the top of the document.
* This will be command + forward slash on mac, or ctrl + forward slash on windows.
* Next we'll import the FunctionalComponent and nest it inside of the return statement in the App function.
* Then we'll pass the TextProp into the FunctionalComponent.

    .. image:: functional-component-props2.*

* From here we'll import the useState hook in order to use state in our functional component.

    .. image:: use-state.*

* Now that we've imported the useState hook we can build out our pieces of state.
* Here we'll be using two separate pieces. One for the styles that we'll pass to the h2, and one to use as our counter.

    .. image:: use-state-2.*

* Notice how syntactically different this is from our previous state in the ClassComponent.
* First our state is defined as a variable, then we have to define a getter, and setter value inside of square brackets
  in order to retrieve state values and set them.
* Then we set it equal to the useState method and pass the desired properties into the method.
* In this next step we'll see how we can use the getter(state) and setter(setState) values.

    .. image:: use-state-3.*

* Some of the syntax looks the same here as it does in the ClassComponent, but notice how we don't have to use this in
  order to access the properties of our state.
* Next we'll pass the state, and the colorChange function into the FunctionalComponent as props so that we can access
  them within the functional component.

    .. image:: use-state-4.*

* Notice how we can use the getter value of the state and pass it as props.
* Next we'll head back to FunctionalComponent.js, and add the code that will allow us to pass these values in and access
  them.

    .. image:: use-state-5.*