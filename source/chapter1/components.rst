React Components
================

As previously stated React components are either functional or class based.

Class Based Components
----------------------

In order to use class based components one must first use the following syntax in order to import the component class
from React.

.. code-block:: javascript

    Import React, { Component } from 'react'


Once that is done we can build a class based component, and it begins to look like the code below. It's important that the
export statement isn't forgotten as this is how components are imported to other components.


.. code-block:: javascript

    Import React, { Component } from 'react'

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

        Import React, { Component } from 'react'

        class ClassComponent extends Component {
            render() {
                return (
                    <div className="container">
				        <header className="header">
				            <h1>Hello World</h1>
				        </header>
                    </div>
                )
            }
        }

   export default ClassComponent
