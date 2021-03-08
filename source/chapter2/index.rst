React Components
================

* Finally we are ready to start coding in React and we'll start off with the basics of components.
* As previously stated components in React can either be functional or class based.

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

Introduction to props
---------------------
* Props or properties are how we transfer data down to child components.
* We can use props to pass many things down in React such as functions, variables, and array objects just to name a few.
* Here we will create a variable that holds a string and pass it down as a prop from the App component to the
  ClassComponent.

    .. image:: prop-variable.*





Functional Components
---------------------

React functional components do not require any import statements at first in their basic form. They are simply defined as
JavaScript arrow functions and take props as a parameter (more on this later).

.. code-block:: javascript

    const header = (props) => {
        render() {
            return (
                <div>

                </div>
            )
        }
    }

   export default ClassComponent

