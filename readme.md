# Kata 006

## Summary
Covers Yarn Workspaces, React/Redux SPA

## Pre Reading
- [Yarn Workspaces](https://yarnpkg.com/en/docs/workspaces)
- [All posts here](http://es6-features.org)

## Discussion
- Install Yarn globally (npm install -g yarn) (done)
- From the workspaces folder, run yarn install (done)
- Example the various folders and package.json files
    https://scotch.io/tutorials/yarn-package-manager-an-improvement-over-npm

    * What are some advantages of Yarn over npm? Advantages of Yarn Workspaces? Some challenges?
    Nested dependencies, Queued install, Single registry, No offline installation
    Workspaces are a new way to setup your package architecture that’s available by default starting from Yarn 1.0. It allows you to setup multiple packages in such a way that you only need to run yarn install once to install all of them in a single pass.
    The package layout will be different between your workspace and what your users will get (the workspace dependencies will be hoisted higher into the filesystem hierarchy)
    https://yarnpkg.com/en/docs/workspaces
    * What are some cross platform package.json challenges?
    os
    This specifies operating system compatibility for your package. It checks against process.platform.
    https://yarnpkg.com/en/docs/package-json
    * Why would someone find a monorepository appealing?
    Using a single repo also reduces overhead from managing dependencies. A side effect of the simplified organization is that it's easier to navigate projects
    * Run yarn web:start. Modify some tsx files in the web project. How can live reloading impact developer productivity?
    Live reloading reloads or refreshes the entire app when a file changes. For example, if you were four links deep into your navigation and saved a change, live reloading would restart the app and load the app back to the initial route
- Research and list pros and cons of TypeScript when it comes to development/quality/testing/builds/and deployments
Pros
Object Oriented Programming Features
TypeScript Does Not Need a Runtime Plugin
Back-end Developer Feel More Comfortable With it
It is Used in Popular Frameworks
Cons
Learning Curve
Needs Development Tooling
- Describe the differences in let/var/const in JS/TS
Var
The JavaScript variables statement is used to declare a variable and, optionally, we can initialize the value of that variable.
let
The let statement declares a local variable in a block scope. It is similar to var, in that we can optionally initialize the variable.
const
const statement values can be assigned once and they cannot be reassigned. The scope of const statement works similar to let statements.
- Describe the differences between arrow functions and normal functions in JS/TS
let x = (parameters) => { 

	// body of the function 

}; 



let square = function(x){ 

return (x*x); 

}; 

console.log(sqaure(9)); 

An arrow function expression is a syntactically compact alternative to a regular function expression, although without its own bindings to the this , arguments , super , or new.target keywords.

- React 16.3 added the Context API, describe how this would work with or without Redux
The Context API is a neat way to pass state across the app without having to use props

## Code Exercise
- Implement a new workspace that uses redux to store data. Describe how you would enhance it to work with async network calls
https://redux.js.org/advanced/async-actions
https://redux.js.org/basics/example
- Augment this with [Redux DevTools](https://github.com/zalmoxisus/redux-devtools-extension)