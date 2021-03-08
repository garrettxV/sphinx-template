React Components
================

Finally we are ready to start coding in React and we'll start off with the basics of components. As previously stated
components in React can either be functional or class based.

Class Based Components
----------------------

In order to use class based components one must first use the following syntax in order to import the component class
from React.

.. code-block:: javascript
    :caption: Importing Component

    import React, { Component } from 'react'


Once that is done we can build a class based component, and it begins to look like the code below. It's important that the
export statement isn't forgotten as this allows for components to be imported to other components and ultimately the final
app component.


.. code-block:: javascript

    import React, { Component } from 'react'

    class ClassComponent extends Component {
        render() {
            return (
                <div>

                </div>
            )
        }
    }

   export default ClassComponent

The return statement inside of the component is where JSX (JavaScript XML) can be used to describe what the UI should
look like, and it closely resembles HTML. It is written mostly like HTML but one of the more immediately identifiable
differences is the fact that className is used to describe a class in JSX instead of class.

.. code-block:: javascript
    :caption: Example of JSX
    :linenos:
    :emphasize-lines: 5,6,7,8,9,10

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

export default ClassComponent;

In order to render this component you should import it to your app component so that it is exported to the
index.html document for rendering. Then you would nest it in the return statement of the App component

.. code-block:: javascript

    import React, { Component } from 'react'
    import ClassComponent from 'filepath goes here '


    class App extends Component {
        render() {
                return (
                    <ClassComponent/>
                )
            }
        }

    export default App;

This would in turn allow your component to be rendered in the index.html document inside of the div with an id of "root".

.. literalinclude:: index.html

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

