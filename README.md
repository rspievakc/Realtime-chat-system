# Real time chat system

## 1. Introduction

&nbsp;&nbsp;The objective of this project is to create a real-time chat solution. I've decided to use Javascript language across all the stack, to unify the language and data format, optimize the development resources, and implement source code re-utilization.

&nbsp;&nbsp;The backend contains REST endpoints and WebSocket channels which implement real-time updates. The REST endpoints will handle user registration, the other services will be accessed by WebSockets.

&nbsp;&nbsp;Please find the sequence diagram link on the section 9.

## 2. Backend technology stack

• **Node.js** - Javascript engine which enables us to use the Javascript language across the stack. Node.js will allow us to build fast and scalable services, and it's capable of handling a vast number of simultaneous connections with high throughput, and its package managers offer a vast ecosystem which makes the development easier.

• **Express.js** - Makes the development of web services and application more straightforward, faster and maintainable. It is easily configurable and customizable, has hierarchical routers, middlewares, and a vast number of libraries which addresses custom requirements on the implementation.

• **Socket.IO** - It is one of the first WebSocket libraries, very popular, has features like rooms, broadcast and message acknowledgment and callbacks. It is very well tested and is production enabled.

• **Redis** - In memory database with Subscribe/Publish channels, which we will be used to implement real-time updates for each user in a distributed architecture. It's very fast and is often used to store cached information, evicting having to compute the same values again.

• **MongoDB** - It is a document database, can use a schema-less model, is very fast, scalable, and has a powerful query engine, and works directly with JSON data.

• **Mongoose** - It is an object document mapper, which translates documents into MongoDB database documents. It implements schema validation and enables a faster development for the MongoDB. It also allows using the chainable query constructor, making the code more readable, flexible and maintainable. There is one disadvantage, the minor degradation in performance since it acts between the service and the MongoDB when compared with direct MongoDB access.

## 3. Frontend technology stack.

• **React** - It is a simple but powerful UI library, with a vast ecosystem. It adheres to the use of componentization, re-utilization, and the one-way data flow. It uses a Virtual DOM to implement a rapid modification detection, introduces a new tag syntax, called JSX, which extends the Javascript, creates a separation of concerns and looks like an HTML syntax.

• **React Native** - It is a compliment for the React ecosystem, targets mobile platforms, works with Android and iOS systems. It generates native applications which will have their Javascript engine, but the UI will be native, fast and with native look and feel.

• **Redux** - It is a well-proven state management engine where the entire application state is managed from a centralized store. The components have direct access to the storage and can update their data when they get changed or update the stored data when required. It makes clean the implementation of very complex projects.

• **Webpack** - It acts as a preprocessor and bundler for all the files related to the UI implementation. It processes all the source files, modules, images, and style sheet and bundles them together, generating a smaller number of artifacts as possible. Along with the React transpiler enabled the hot reload of the application, saving time for the developer.

• **SCSS** - It is the new syntax to implement cascading style sheets (SASS 3), is fully compatible with the plain CSS syntax, performs new features, enables the creation of hierarchical rules, more readable code, and knows almost all the browser quirks and vendor syntaxes.

• **React-Semantic-UI** - It is a UI framework which easies the UI implementation, it is stunning, creates a modern look and feel, modular,  and has many UI components and integrates easily with the React.

• **Socket.IO** (client) - It is the counterpart for the Socket.io used on the service. As already mentioned it helps to implement real-time updates through the use of WebSockets.

## 4. Infrastructure

• **Docker** - It is a containerized solution for developing, shipping and running applications. It detaches de application from the infrastructure enabling us to create image, containers and to deliver the solution quickly. It also allows us to use containers in the developer workstations, replicating the production environment. The docker's containers define the unit for distribution and allow to scale our services efficiently.

• **Kubernetes** - It offers us the Docker containers orchestration, including deployment, scaling, and management, also,  it is independent of the infrastructure provider.

## 5. Development tooling

• **Visual Studio Code** - It is Open Source, runs in all OSes, has a vast ecosystem of plugins, multiple language support, embedded debugging, extensive tooling and makes developing software more accessible.

• **Git and GitHub** - It is an open-source version control system, used worldwide which allow us to track the application's code change and share the source base with as many developers we need.

• **Chrome Browser** (latest) - One of the best browsers available at the moment, has a vast number of plugins which help the debugging process. We will be using the Redux DevTools and React DevTools.

## 6.  Testing, Integration, Deployment, Scaling and Monitoring

We are going to use the Kubernetes for container orchestration. There will be separated clusters for the Backend services, MongoDB, and Redis databases.

A Jenkins setup will handle the continuous deployment and integration. Jest, Chai, and Mokka will be utilized to create test cases for the system.

We are going to create a cluster for the **ELK** (Elastic search, Logback, and Kibana) stack deployment to collect the logs from all the clusters, which are going to be feed to the Logback instance and processed by the Elastic search. The Kibana will be used to create the dashboard(s) for monitoring and the alert system.

The container instance will send their keep alive with the instance CPU and Memory resources utilization, which are going to be processed by the **ELK** stack and presented on the Kibana dashboards.

There will be four sets of clusters, one for the development cycle, one for the testing cycle, on for the pre-release period, and one for production deployment. We can also create a temporary cluster for the bug fixing cycle.

## 7. Collaboration and Project Management

We are using the Asana Project Management system to create a collaborative development platform. It will handle tasks, issues, chronograms, and documentation snippets.\
The GitHub platform is going to handle the version-control for the system and will be integrated on the Asana platform.

## 8. New feature: Message search system.

The ELK stack can be extended to implement the message searching feature. The idea is to index all the groups/rooms and their respective messages allowing the user to search past messages.\
As an option, we can also create a message classification system, which can flag essential messages.

## 9. Attachments

  [Sequence Diagram](./Sequence_diagram.pdf)











	
		
	
		
	