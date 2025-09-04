# Flash Cards

## Utvecklingsprocess & Metodik

### Continuous Monitoring
The practice of constantly tracking, analiyzing and reporting the performance, security and reliability of an application or system in real-time. This process helps to identify and resolve issues before they affect end users, ensuring the application runs smoothly. Continuous monitoring typically involves tracking metrics such as system health, uptime, response times, error rates, and security threats.

### CI (Continuous Integration)
A software development practice where developers frequently integrate their code changes into a shared repository, typically several times a day. Each integration is automatically buit and tested to detect errors as early as possible. CI aims to improve the quality of the code, reduce integration problems, and allow teams to develop cohesive software rapidly.

### DRY (Don't Repeat Yourself)
A principle of software development aimed at reducing repetition of code, logic, or data within a system. The DRY principle encourages developers to avoid duplicating code by abstracting repeated logic or data into reusable components, functions, or modules. This approach promotes cleaner, more maintainable code, and reduces the risk of errors by ensuring that any change only needs to be made in one place.

### Self-Organizing Team
A group of individuals who manage their work and responsibilities autonomously without the need for centralized control or micromanagement. In a self-organizing team, members collectively decide how tasks are distributed, how goals are met, and how problems are solved, leveraging their skills and expertise to achieve the best outcomes. This concept is central to agile methodologies like Scrum and is designed to foster collaboration, accountability, and adaptability.

### Test-Driven Deployment (TDD)
A software development process in which developers write tests for a new feature or functionality before writing the actual code to implement it. The TDD cycle typically involves writing a failing test, writing the minimum code necessary to pass the test, and then refactoring the code while ensuring that all tests continue to pass. TDD promotes the creation of cleaner, more reliable code by ensuring that every piece of functionality is backed by a corresponding test.

### End User Testing (also known as User Acceptance Testing or UAT)
The final phase of the software testing process where the actual users of the software test the system in a real-world environment to ensure that it meets their needs and requirements. This type of testing focuses on validating that the software performs as expected from the user's perspective, addressing both functionality and usability before the product is released to production.

### Deployment Pipeline
A series of automated steps that software goes through as it progresses from development to production. The pipeline typically includes stages such as building the application, running unit and integration tests, deploying to a staging environment for further testing, and finally, deploying to the production environment. Each stage in the pipeline ensures that the code is thoroughly tested and verified, reducing the risk of errors or bugs reaching the production environment. The pipeline is a critical component of Continuous Integration (CI) and Continuous Delivery (CD) practices, enabling faster and more reliable software releases.


---

## Arkitektur & Systemdesign

### Frontend System
Refers to the collection of tools, libraries, frameworks, and technologies used to build the user-facing part of a web application or website. This system is responsible for everything users interact with directly in their web browsers, including the user interface, navigation, content rendering, and dynamic behavior. A robust frontend system ensures a responsive, interactive, and seamless user experience across different devices and platforms.

### Serverless Computing
A cloud computing model where the cloud provider automatically manages the infrastructure, allowing developers to focus solely on writing and deploying code. In a serverless architecture, the server management and capacity planning are abstracted away, and the cloud provider dynamically allocates resources as needed. Developers deploy functions, which are small, independent pieces of code that execute in response to specific events. Popular serverless platforms include AWS Lambda, Azure Functions, and Google Cloud Functions.

### Microservice
An architectural style that structures an application as a collection of loosely coupled, independently deployable services. Each microservice is responsible for a specific piece of functionality, such as user authentication, payment processing, or product management, and communicates with other services over a network, typically using HTTP/REST, gRPC, or messaging queues. This approach contrasts with monolithic architectures, where all functionality is tightly integrated into a single application.

### Twelve Factor App
A methodology for building modern, scalable, and maintainable software-as-a-service (SaaS) applications. It was introduced by developers at Heroku to provide best practices for building web applications that can be easily deployed and scaled in cloud environments. The methodology outlines twelve principles that address various aspects of software development, from codebase management to deployment and operational concerns.

### Multi-Tier Architecture (also known as n-Tier Architecture)
A software architecture pattern that separates an application into multiple, distinct layers or tiers, each responsible for specific aspects of the application's functionality. This separation of concerns helps to organize code, improve scalability, and manage complexity by allowing each tier to evolve independently. The most common form is a three-tier architecture, but applications can have more or fewer tiers depending on the design requirements.

### Environment Variables
In React, Environment Variables are special variables that are used to configure different aspects of the application depending on the environment (development, production, testing, etc.). These variables can control things like API endpoints, feature toggles, and other settings that may need to vary between environments. Environment variables in React are defined ina`.env` file and are typically prefixed with`REACT_APP_` to ensure they are properly recognized and injected into the React application at build time.

### Prod Environment
The Production Environment (Prod) is the live environment where the final version of a software application is deployed and made available to end users. is the most critical environment in the software development lifecycle, as it serves real users and handles actual data. The production environment is optimized for performance, reliability, and security, ensuring that the application runs smoothly under real-world conditions.

### Dev environment (Development Environment)
Where software developers write, test, and debug their code. This environment is typically isolated from production and other environments, allowing developers to make changes freely without affecting end users. The dev environment is set up to mimic the conditions under which the code will eventually run, but it is often less restrictive and may include debugging tools, detailed logs, and hot-reloading capabilities that make development faster and more efficient.

### Environment
In software development, an Environment refers to a distinct setup of hardware, software, and configuration settings where specific stages of the software lifecycle, such as development, testing, or production, are carried out. Different environments are used to isolate and manage changes in the application at various stages, ensuring that the software behaves correctly before it is released to end users.


---

## Programmering & Kodning

### Interpreter (in comparison with Transpiler and Compiler)
An Interpreter is a type of program that directly executes instructions written in a programming or scripting language without requiring them to be compiled into machine code first. Instead of translating the entire source code into a lower-level language (as a compiler does), an interpreter processes the source code line by line or statement by statement, translating and executing it on the fly. This can lead to slower execution times compared to compiled languages, but offers the advantage of immediate execution and ease of debugging.

### API (Application Programming Interface)
A set of rules that allows different software applications to communicate with each other.

### Persistency
In JavaScript, persistency refers to the ability to store data in a way that it remains available across different sessions, application restarts, or system reboots. Persistent storage ensures that data is not lost when a user closes their browser or when a server shuts down, making it crucial for maintaining state, user preferences, and application data over time.

### CommonJS
A module system for JavaScript, primarily used in server-side development with Node.js. It allows developers to structure their code into reusable modules, making it easier to manage dependencies and maintain large codebases. Modules in CommonJS are loaded synchronously using the require` function, and they export their functionality using`module.exports`.

### Client-Side Scripting
Refers to the execution of scripts, typically written in languages like JavaScript, within the user's web browser rather than on the server. This allows web pages to be dynamic, interactive, and responsive to user input without requiring a page reload. Common tasks for client-side scripts include form validation, DOM manipulation, and making asynchronous requests to a server (AJAX).

### Hot Module Replacement (HMR)
A feature in modern web development tools that allows modules of an application to be updated in the browser without requiring a full page reload. This feature is particularly useful during development, as it enables faster iteration by instantly applying changes to the application's code while preserving the current state.

### Require
`require` is a function in Node.js, used as part of the CommonJS module system, to synchronously load and use modules. It allows you to import functionality from other files or modules into your current file. Unlike the ES6 `import`statement, `require` can be called conditionally and at any point in the code, making it flexible but synchronous in nature. `require` is primarily used in Node.js environments to load CommonJS modules.

### Node
Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to execute JavaScript code on the server side. Built on Chrome's V8 JavaScript engine, Node.js is designed for building scalable, highperformance applications, particularly those that require real-time data interaction, such as web servers, APIs, and streaming services. Node.js uses an event-driven, non-blocking I/O model, making it efficient and suitable for applications that handle a large number of simultaneous connections.

### Express
Express.js is a minimal and flexible web application framework for Node.js. It provides a robust set of features for building web and mobile applications, including tools for routing, middleware management, and handling HTTP requests and responses. Express.js simplifies the process of creating serverside applications, allowing developers to focus on writing the business logic rather than dealing with the underlying infrastructure.

### CommonJS
A module system for JavaScript, primarily used in server-side development with Node.js. It allows developers to structure their code into reusable modules, making it easier to manage dependencies and maintain large codebases. Modules in CommonJS are loaded synchronously using the require` function, and they export their functionality using`module.exports`.

### Server-Side Scripting
The process of writing code that runs on a server rather than on the client (browser). This scripting is responsible for generating dynamic web content, interacting with databases, handling user requests, and managing application logic before sending the final output to the client's browser. Common server-side scripting languages include PHP, Node.js (JavaScript), Python, Ruby, and Java.

### Import (ES6 Modules)
A statement in JavaScript used to bring in modules and their exports from other files into the current file. It is part of the ES6 module system, which is designed to allow for modular programming and code reuse. Unlike` require, `import` is statically analyzed, meaning it is hoisted and processed before the rest of the code runs. `import` supports both named imports and default imports, and while it is usually static, dynamic imports are also possible using `import()`.

### ECMAScript 6 (ES6)
ES6, also known as ECMAScript 2015, is the sixth edition of the ECMAScript language specification, and it brought significant updates to JavaScript. ES6 introduced new features and syntax that improved the language's power, readability, and ease of use, especially for building complex applications. Browser Support: Modern browsers have largely adopted ES6 features, but older browsers may require transpilation (e.g., using Babel) to convert ES6 code into ES5, ensuring compatibility.


---

## Testning

### Cypress
A modern, end-to-end testing framework designed specifically for web applications. It allows developers to write tests that run directly in the browser, simulating user interactions and verifying that the application behaves as expected. Cypress is known for its fast execution, real-time reloading, and built-in dashboard that provides detailed insights into test results. It's particularly popular for testing complex JavaScript applications built with frameworks like React, Angular, and Vue.js.

### Component Testing
Involves testing individual components of a software application in isolation to ensure they function correctly. This type of testing treats the component as a "black box," focusing on the inputs and expected outputs without considering the internal workings. It's commonly used in the context of Ul components in frameworks like React, where you test how a specific component behaves under various conditions.

### Mock (Testing Double)
A type of testing double used in software testing that not only simulates the behavior of real objects but also records the interactions with it, such as method calls and arguments passed. Mocks are particularly useful when you need to verify that certain methods were called during the execution of a test and to check the specific interactions between components. Mocks can be pre-programmed with expectations that define what methods should be called and with what parameters, making them more sophisticated than other testing doubles like stubs or dummies.

### Integration Testing
A level of software testing where individual units or components are combined and tested as a group. The primary goal of integration testing is to identify issues that occur when different components interact with each other, such as mismatches in data formats, incorrect interfaces, or unexpected behavior when units are integrated. This type of testing ensures that the components of a system work together as expected and that their interactions produce the correct results.

### Stub (Testing Double)
A type of testing double used in software testing that replaces a real object or method with a simplified version that provides predefined responses. Unlike mocks or spies, stubs do not record interactions or track how they are used; they simply return hard-coded values or responses when called. Stubs are particularly useful when you need to isolate the component under test by removing dependencies on external systems or complex objects, ensuring that the test focuses solely on the logic being tested.

### Jest
A popular JavaScript testing framework developed by Facebook, designed primarily for testing React applications, but also suitable for any JavaScript project. Jest provides a powerful, flexible, and easy-to-use environment for writing and running tests. It includes features like zeroconfiguration setup, an easy-to-understand syntax, built-in mocking capabilities, and snapshot testing. Jest also supports testing asynchronous code and has a rich set of matchers for assertions.

### Doubles
Dummy: Used to fill parameters, not actually used. Fake: A simplified working implementation (e.g., in-memory database). Spy: Records method calls and parameters for later verification. Stub: Provides predefined responses, used for testing in isolation. Mock: Verifies interactions with expectations, used to test behavior.

### Unit Testing
A software testing method where individual units or components of a software application are tested in isolation from the rest of the application. The primary goal of unit testing is to verify that each unit functions correctly on its own. Unit tests are typically written and run by developers and are known for being fast and efficient, providing quick feedback on the correctness of the code during development.

### Double Dummy
In software testing, a Dummy is a type of testing double used as a placeholder object that is passed around but never actually used in the test. Dummies are typically utilized when a method or function requires an argument, but the specific value of that argument is irrelevant to the test being conducted. The primary purpose of a dummy is to fulfill the requirements of the function signature without influencing the outcome of the test.

### React Testing Library
A lightweight testing utility that provides tools for testing React components. Unlike traditional testing frameworks, React Testing Library focuses on testing components from the perspective of the user, ensuring that your tests are more reliable and maintainable by simulating user interactions and verifying the behavior of the component as it would be in a real environment. It is often used in conjunction with testing frameworks like Jest.

### Fake (Testing Double)
A type of testing double used in software testing that provides a working, but simplified, implementation of a component or service. Unlike dummies or stubs, which do not carry out any real logic, a fake mimics the behavior of a real object but with less complexity, making it suitable for testing purposes. Fakes are often used when the real object is too resource-intensive complex to use in a test environment, such as a database or an external API.

### Spy (Testing Double)
A Spy is a type of testing double used in software testing that wraps around a real object or function and records information about how it is used during the test, such as method calls and the arguments passed. Unlike mocks or stubs, a spy does not replace the original functionality; instead, it monitors and tracks interactions without altering the behavior of the underlying code. Spies are particularly useful for verifying that certain methods were called, how many times they were called, and with what parameters, while still allowing the original logic to be executed.


---

## Deployment & Infrastruktur

### Dependency Management
Dependency Management in a React application refers to the process of handling the libraries and packages that your project relies on, ensuring they are correctly installed, updated and configured. This is typically managed through the 'package.json' file, which lists all the dependencies required for the project. Tools like npm (Node Package Manager) or Yarn are used to automate the installation, updating and removal of these dependencies, making it easier to maintain a consistent development environment across different machines.

### Deploy
Deployment is the process of moving an application or its components from one environment to another, typically from development (dev) to testing (test), staging (stage), and finally to production (prod). Each environment serves a specific purpose: dev for development, where code is actively written and modified; test for quality assurance and automated testing; stage for final verification in an environment that closely mirrors production; and prod where the application is made available to end users. Deployment can involve several steps, including building the application, running tests, and transferring the application to the target servers.

### Containerization
A lightweight form of virtualization that involves packaging an application along with its dependencies, libraries, and configuration files into a single, portable container. This container can run consistently across different environments, from development to production, regardless of underlying system differences. Containers are isolated from each other and the host system, but they share the host's operating system kernel, making them more efficient than traditional virtual machines.

### Environment Variables
In React, Environment Variables are special variables that are used to configure different aspects of the application depending on the environment (development, production, testing, etc.). These variables can control things like API endpoints, feature toggles, and other settings that may need to vary between environments. Environment variables in React are defined ina`.env` file and are typically prefixed with`REACT_APP_` to ensure they are properly recognized and injected into the React application at build time.

### Deployment Pipeline
A series of automated steps that software goes through as it progresses from development to production. The pipeline typically includes stages such as building the application, running unit and integration tests, deploying to a staging environment for further testing, and finally, deploying to the production environment. Each stage in the pipeline ensures that the code is thoroughly tested and verified, reducing the risk of errors or bugs reaching the production environment. The pipeline is a critical component of Continuous Integration (CI) and Continuous Delivery (CD) practices, enabling faster and more reliable software releases.

### Docker
A platform for developing, shipping, and running applications inside lightweight, portable containers. These containers bundle the application code along with its dependencies, libraries, and configuration files, ensuring that the application runs consistently across different environments, whether on a developer's laptop, on-premise servers, or in the cloud. Docker simplifies the deployment process by allowing developers to package everything the application needs to run into a single container, avoiding the "it works on my machine" problem.

### Merge Conflict
A Merge Conflict occurs when Git is unable to automatically resolve differences between two branches during a merge. This typically happens when changes are made to the same part of a file in different branches, and Git cannot determine which change should take precedence. Merge conflicts must be resolved manually by the developer before the merge can be completed.


---
