Components
==========

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

