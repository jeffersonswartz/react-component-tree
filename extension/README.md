<!-- SAPLING README -->
<!-- NOTE: this README is the one that shows inside VSCode extension marketplace -->

<!-- PROJECT LOGO -->
<br />
This project is forked from https://github.com/oslabs-beta/sapling but it seems the project is dead, we have made a lot of core performance improvements
and will continue to add new features. 
<p align="center">
  <a href="https://github.com/hb1998/react-component-tree">
    <img src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/logo.png" alt="Logo" height="120">
  </a>

  <h2 align="center">React component tree</h2>

  <p align="center">
    A convenient way to traverse your React application.
    <br />
    <a href="https://github.com/hb1998/react-component-tree"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/hb1998/react-component-tree/issues">Report Bug</a>
    ·
    <a href="https://github.com/hb1998/react-component-tree/issues">Request Feature</a>
  </p>
  
</p>

<hr>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#installation">Installation</a></li>
    <li>
      <a href="#getting-started">Getting Started</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#extension-settings">Extension Settings</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#creators">Creators</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<hr>

## About The Project

<br/>
<p align="center">
  <img width="900" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/quizwall_demo.gif">
</p>
<br/>

React component tree is a VS Code extension built with React developers in mind. As your codebase grows, your native file structure becomes less and less intuitive. Wouldn't it be nice to have a file structure that represents the actual relationships between the components and containers in your application? Wouldn't you like a quick reference to your available props, and an indication of routes and conditional rendering?

With React component tree, you don't have to guess at the parent component of your current file. React component tree is an interactive hierarchical dependency tree that lives directly within your VS Code IDE, as accessible as the native file system. You can build your tree by selecting any component file as the root and get information about the available props at any level. It also provides visual indication of Javascript syntax or import errors in your files, and shows you which components are connected to your Redux store.


### Built With
<ul>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/react-brands.png"><a href="https://reactjs.org/"> React</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/vscode.png"><a href="https://code.visualstudio.com/api"> VSCode Extension API</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/mochajs-icon.png"><a href="https://mochajs.org/"> Mocha</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/chai_icon.png"><a href="https://www.chaijs.com/"> Chai</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/babel-logo-minimal.png"><a href="https://babeljs.io/docs/en/babel-parser"> Babel Parser</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/webpack.png"><a href="https://webpack.js.org/"> Webpack</a>
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/github-actions.png"><a href="https://github.com/features/actions"> GitHub Actions</a>
  </li>
</ul>

## Installation

Installing from VS Code Extension Marketplace:

1. If needed, install Visual Studio Code for Windows (7+), macOS (Sierra+), or Linux (details).

2. Install the React component tree extension for Visual Studio Code. Search for 'sapling' in the VS Code extensions tab, or click [here](https://marketplace.visualstudio.com/items?itemName=team-sapling.sapling).

3. Once complete, you'll see React component tree appear in your sidebar. You can now begin using React component tree! Check out the Getting Started below for information on how to get started.

To install sapling for development, please see the contributing section below.

## Getting Started

1. After installing VSCode Extension, you will see the extension on your sidebar. Click the "Choose a File" button.

2. Your file explorer window will launch. Select an entrypoint, a file where the parent component for the rest of your application is rendered.

3. Your sidebar will now display a component tree.

## Usage

After installing, click the React component tree tree icon in your extension sidebar (image of icon here). From there, you can either click "Choose a file" to select your root component, or build your tree directly from a file open in your editor with the "Build Tree" button on the right hand side of your status bar. Click the + and - buttons to expand and collapse subsets of your tree, and hover over the information icon (image of icon here) to get a list of props available to that component. You can also press the view file icon (image of icon here) to open the file where the component is defined in your editor window. Below is a quick-reference legend for icon and text format meanings. If you prefer not to view React Router or other third-party components imported to your app, you can disable either of these in the VS Code Extension Settings.

Icon Legend in React component tree Tree View:
<ul>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/circle-info-solid.png">  available props (hover)
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/circle-arrow-right-solid.png" >  open file (click)
  </li>
  <li>
    <img height="14" src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/store-solid.png" >  Redux store connection
  </li>
  <li>
    <span color="red">Navbar</span>  error in file (matches the error color of your theme)
  </li>
  <li>
    <b>Navbar</b>: currently open file
  </li>
</ul>

React component tree can currently display React apps made with JSX/TSX and ES6 import syntax.

React component tree will detect React components invoked using JSX tag syntax and React-Router component syntax, where React is imported in a file:

```JSX
    // Navbar will be detected as a child of the current file
    <Navbar />

    // As above
    <Navbar></Navbar>

    // Route and Navbar will be detected as child components of the current file
    <Route component={Navbar} />

    // Route and App will be detected as child components of the current file
    <Route children={App} />
```

React component tree will detect the names of inline props for JSX components it identifies:

```JSX
    // props 'userId' and 'userName' will be listed for Navbar in React component tree
    <Navbar userId={...} userName={...} />
```

React component tree can identify components connected to the Redux store, when 'connect' is imported from 'react-redux', and the component is the export default of the file:

```JSX
    // App.jsx
    import React from 'react';
    import { connect } from 'react-redux';

    const mapStateToProps = ...
    const mapDispatchToProps = ...

    const App = (props) => {
      return <h1>This is the App</h1>
    }

    // React component tree will detect App as connected to the Redux store
    export default connect(mapStateToProps, mapDispatchToProps)(App);
```

### Note
React component tree prioritizes file dependencies over component dependencies. Consider the following JSX contained in the file App.jsx:

```JSX
    // App.jsx
    import React from 'react';
    import Home from './Home';
    import Navbar from './Navbar';

    class App extends Component {

      render (
        return {
          <Home>
            <Navbar />
          </Home>
        })
    }
```

React component tree will display Home and Navbar as siblings, both children of App: (image of actual React component tree here)

<br />
  <img src="https://raw.githubusercontent.com/hb1998/react-component-tree/master/extension/media/readme-example.png">

## Extension Settings

This extension contributes the following settings:

* `sapling.view.reactRouter`: enable/disable React Router component nodes
* `sapling.view.thirdParty`: enable/disable all third party component nodes

## License

Distributed under the MIT License. See [`LICENSE`](https://github.com/hb1998/react-component-tree/blob/master/LICENSE) for more information.

## Creators

* [Habeeb](https://github.com/hb1998)
* [Arul Valan](https://github.com/ArulValan)
* [Charles Gutwirth](https://github.com/charlesgutwirth)
* [Jordan Hisel](https://github.com/jo-cella)
* [Lindsay Baird](https://github.com/labaird)
* [Paul Coster](https://github.com/PLCoster)


## Acknowledgements
* Parsing Strategy inspired by [React Component Hierarchy](https://www.npmjs.com/package/react-component-hierarchy)
* Interactive tree view styling adapted from [Pure CSS Tree Menu](https://codepen.io/bisserof/pen/fdtBm)
* Icons from [Font Awesome](https://fontawesome.com)
* Tooltips with [Tippy](https://www.npmjs.com/package/@tippy.js/react)
* [Best README Template](https://github.com/othneildrew/Best-README-Template)
* React component tree Logo from [Freepik](https://www.freepik.com/vectors/tree)
* Readme badges from [shields.io](https://shields.io/)