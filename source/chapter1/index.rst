Getting Started With React
==========================

What is React?
--------------

* React is a JavaScript library that is used to build user interfaces.

* React runs on the client as a single page application, and can be used to build full stack applications, which is an
  application that includes both front end and back end code, and code that links the front end to the back end.

* Backend code is server side code which involves the code that communicates between the database and the browser.

* Front end code involves coding the user interface, which is what the user interacts with directly and that's what will
  be dealt with in this tutorial.

* React is component based and each component manages it's own state.

* Components are used in conjunction with one another to create complex user interfaces.

* Components can be functional components, or class based components. Functional components are
  considered to be stateless components whereas class based components are stateful components.

* There is a one way flow of data in React applications where data flows from parent to children.

* Data is transferred to children through props which is short for properties.

* State is an object that controls how a component renders based on a change in the data,
  and it can be passed down through props in order to control it from children components.

What This Tutorial Will Cover
-----------------------------

* Getting started with building react components (functional and class based).
* Integrating components with other components through imports and nesting.
* Examples of styling components with inline css in JSX (JavaScript XML), Styling with JavaScript variables, and
  importing regular old CSS files into components.
* The use of props in order to transfer data to child components with various examples.
* The use of state in order to control how a component renders with various examples.
* Passing state as props.
* React Router which is a React library that can be used to control the rendering of components through links the omit
  the necessity of a page refresh.




Requirements
------------

In order to set up a React environment you first need to install a `couple of things <https://docs.npmjs.com/downloading-and-installing-node-js-and-npm>`_.
There are details on these requirements in the next section.

    1. Node.js >= 10.16
    2. npm >= 5.6

First you should check whether or not Node.js and npm are already installed. in order to do this we can check with the
following commands in the command prompt or terminal. These commands will tell you whether or not each are installed by
displaying which versions you have.

    .. literalinclude:: node.txt
        :caption: Node version command.

    .. literalinclude:: npm.txt
        :caption: NPM version command.

If these requirements are not installed or your current versions aren't up to snuff then run the following command in
order to install or update each. This will install each globally on your machine.

    .. literalinclude:: node_npm_install.txt
        :caption: Node and NPM installation global command.




What are Node.js, NPM, and Create React App
----------------------------------

* Node.js is a JavaScript runtime environment that contains everything that is necessary in order to execute programs
  written in JavaScript.
* Node.js took JavaScript from a language that could only be ran in the browser to a language that has the capability to
  run locally on your machine in standalone applications.
* Node package manager, or npm contains packages that are used in order to make development faster and more efficient.
* Many npm packages are often used throughout the development of React applications.
* After installing Node.js along with npm you can set up your React environment by using `create react app <https://reactjs.org/docs/create-a-new-react-app.html>`_
  which is a CLI, or command line interface tool that allows you to create a project folder that essentially contains
  all of the files, folders, and packages that you'll need in order to hit the ground running with React. It makes
  starting a React project simple and takes out the complexities of configuring and making sure that you have all of the
  correct requirements.
* It will also come packaged with a development server via a localhost which is a server environment in which your
  computer acts as a server.
* you'll also need to use `npx <https://www.educative.io/edpresso/what-is-npx>`_ which is a tool used to run registered
  node executables that would normally have to be installed via npm.
* It is installed along with npm version 5.2 or greater.
* NPX will check to see if packages that you're attempting to use are already installed, and if they're not they will be
  downloaded.
* The following commands will be used in order to set up your React environment (these are referred to in `create react app <https://reactjs.org/docs/create-a-new-react-app.html>`_)
  and these commands will be executed in the terminal or command line on your machine.
* In the following example my-app refers to the name of your application folder, which can be any name that you choose.

    .. literalinclude:: info.txt
        :caption: Create React App commands

* In the above commands npx is used in order to allow easy access to the create react app CLI.
* the create react app CLI sets up your React environment and that environment is given a name.
* Once these commands are completed you should have changed directories into your application folder and you should see
  the following in your browser.


    .. image:: react-app_png.*


* If you see the page above in your browser you're now running your react app from your localhost server.
* In order to get started with actually building your application you'll need to install a text editor if you haven't
  already, and open your app directory in the text editor.
* I recommend `Visual Studio Code <https://code.visualstudio.com/>`_ for this purpose, and that's what will be used for
  remainder of the tutorial.

Visual Studio Code
------------------

* After you've managed to install Visual Studio Code through the link provided above open the application.
* Next you should see a welcome page and under start you'll see open folder click that and locate your React app
  directory on your machine.
* Click the directory folder and click open.
* Now you should see the following in Visual Studio Code.


    .. image:: Welcome-React-Tutorial.*


Clean Up
-----------------

Now we'll set up our React environment by doing some cleanup and installing some necessary packages that we'll use
throughout the course of this tutorial. The use of Create React App is a great convenience, but it does require some
sprucing up. In the next steps of this tutorial we'll do just that.

* Deletion of the yarn.lock file as we'll be using npm for this tutorial.
* Yarn is a package manger much like npm but we'll be focusing on the use of npm, and using both yarn and npm together
  is subject to conflicts.
* To do this locate the yarn.lock file under the explorer as shown in the image below.


    .. image:: yarn-lock.*


* To delete yarn.lock right click and select delete.
* Next we'll open the index.html file located inside of the public folder. Upon opening we'll see our html boiler plate
  code


    .. image:: index-html.*


* Here we'll want to remove all the commented out text along with all of the link tags. Also go ahead and remove the meta
  tag that includes the theme-color. When you're finished it should look like the image below.
* Also inside the title tag you can give the application a title that seems fitting to you.
* Here you'll also notice a div with an id of "root". This is the container that will hold our react application. It's
  how we actually display the contents of our app in the browser.


    .. image:: clean-up-html.*

* Next referring to the image above where we deleted yarn.lock we'll want to delete the two .png images in the public
  folder along with favicon.io, and robots.txt.
* Upon completion of that (again referring to the image where we deleted yarn.lock) we'll then want to delete app.test.js
  in the src folder along with app.css and setupTests.js. They won't be necessary for this tutorial. Don't be alarmed if
  it fails to compile at this point as it is normal and we'll fix this in the next step.
* Next we'll open up App.js which is located in the src folder and clean that up by removing the two import statements
  at the top of the document along with everything inside of the div with a className of App. Upon completion of that
  App.js should look like the image below.


    .. image:: App-function.*

If you've followed all of the steps correctly the code should compile and you should see a blank screen in the browser.

Package Installation
--------------------

Next we'll go ahead and install a package that will be necessary for this tutorial, and this package is `React Router Dom <https://www.npmjs.com/package/react-router-dom>`_

* React Router will be solely used in this case to seamlessly route between components without the need for a page refresh
  and if you are curious about delving into it more you can refer to `this link <https://reactrouter.com/web/api/Route/exact-bool>`_.
* In order to install React Router Dom you'll need to open a new terminal in Visual Studio.
* You can do this by locating terminal in the toolbar. Click terminal and select open new terminal.
* Also here's a couple of links for VS Code shortcuts for convenience. This one's for `Windows <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf>`_,
  and this one's for `Mac <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf?WT.mc_id=code-online-jopapa>`_.
* Next you'll type in the following command which will use npm to install react router dom package.

    .. literalinclude:: react-router.txt
        :caption: Install React Router

* Upon completion of the installation locate the package.json file at the bottom of your src folder and open it.
* Upon opening you should see that react-router-dom has been added to the list of dependencies.

    .. image:: package-json.*






