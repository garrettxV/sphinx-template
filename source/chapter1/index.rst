Intro to React
==============

React is a JavaScript library that is used to build user interfaces. React runs on the client as a single page
application, and can be used to build full stack applications, which is an application that includes both front end and
back end code, and code that links the front end to the back end. Backend code is server side code which involves the code
that communicates between the database and the browser. Front end code involves coding the user interface, which is
what the user interacts with directly and that's what will be dealt with in this tutorial. React is component based and
each component manages it's own state (more on state later). Components are used in conjunction with one another to create
complex user interfaces. Components can be functional components, or class based components. Functional components are
considered to be stateless components whereas class based components are stateful components.

Requirements
------------

In order to set up a React environment you first need to have Node.js >= 10.16 and npm >= 5.6 installed. In order
to do this refer to `this link <https://docs.npmjs.com/downloading-and-installing-node-js-and-npm>`_. Node.js is a JavaScript runtime
environment that contains everything that is necessary in order to execute programs written in JavaScript. Node.js took
JavaScript from a language that could only be ran in the browser to a language that has the capability to run locally on
your machine in standalone applications. Node package manager, or npm contains packages that are used in order to make
development faster and more efficient. Many npm packages are often used throughout the development of React applications.

After installing Node.js along with npm you can set up your React environment by using `create react app <https://reactjs.org/docs/create-a-new-react-app.html>`_ which is a CLI,
or command line interface tool that allows you to create a project folder that essentially contains all of the files, folders, and
packages that you'll need in order to hit the ground running with React. It will also come packaged with a development
server via a localhost which is a server environment in which your computer acts as a server. you'll also need to use
npx which is a tool used to run registered node executables that would normally have to be installed via npm. It is
installed along with npm version 5.2 or greater. NPX will check to see if packages that you're attempting to use
are already installed, and if they're not they will be downloaded. The following commands will be used in order to set
up your React environment and these commands will be executed in the terminal or command line on your machine. In the example
my-app refers to the name of your application folder, which can be any name that you choose.

    .. literalinclude:: info.txt

In the above commands npx is used in order to allow easy access to the create react app CLI. the create react app CLI
sets up your React environment and that environment is given a name. Once these commands are completed you can now cd
or change directory into your application directory or folder. Once you're in your application directory you can now
run the command npm start which will allow you to view your React application from your localhost server. In order to get
started with actually building your application you'll need to install a text editor if you haven't already, and open
your app directory in the text editor. I recommend `Visual Studio Code <https://code.visualstudio.com/>`_ for this purpose,
but you can use any text editor that you'd like.


