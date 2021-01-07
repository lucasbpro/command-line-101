# React.js

### Install Node.js

To build a React application, you first need to install [Node.js](https://nodejs.org/en/) on your machine.

After installation of Node.js, _npm_ and _npx_ commands (NPM is the Javascript package manager) will be available in the terminal.

### Setting up a React app

To create a default React application, we use [Create-React-App](https://create-react-app.dev/) to set up a standard React project via the command below
```shell
$ npx create-react-app <NAME_OF_YOUR_APP>
```
The command above will take some time to complete. At the end, it will create a full and functional React application which is stored in a folder named <NAME_OF_YOUR_APP> within your current working directory. 

To start the application on [http://localhost:3000](http://localhost:3000), you then run

```shell
$ cd  <NAME_OF_YOUR_APP>
$ npm start
```

### Adding dependencies to your React project

```shell
$ npm install <name_of_dependency>
```

OR 

```shell
$ yarn add <name_of_dependency>
```
