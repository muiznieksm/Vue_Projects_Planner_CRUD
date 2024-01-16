
# Project Planner CRUD
This is a project planner application built with Vue.js. It utilizes Vue Router for navigation and relies on a mock backend provided by json-server.

## Getting Started
These instructions will guide you through setting up and running the application on your local machine for development and testing purposes.

### Prerequisites
Before running this project, ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [npm (Node Package Manager)](https://www.npmjs.com/)
- [Vue CLI](https://cli.vuejs.org/)

### Installation
Follow these steps to set up the project environment:

#### Step 1: Install Dependencies
Run `npm install` in the project directory to install all the required dependencies.

```
npm install
```

#### Step 2: Start the Vue Development Server
Execute `npm run serve` to start the Vue development server. This will compile the application and serve it usually at [http://localhost:8080](http://localhost:8080).

```
npm run serve
```

Navigate to [http://localhost:8080](http://localhost:8080) in your browser to view the application.

#### Step 3: Run the Mock Backend Server
To set up and run the mock backend server, execute the following command. This starts json-server on the specified port, watching changes to `db.json`.

```
npx json-server --watch db.json --port 3001
```

## Features
- Project planning and management functionalities
- Vue Router for single-page application navigation
- Integration with json-server for a mock backend
- Comprehensive project management and tracking features

## Built With
- [Vue.js](https://vuejs.org/) - The progressive JavaScript framework used
- [Vue Router](https://router.vuejs.org/) - The official router for Vue.js
- [json-server](https://github.com/typicode/json-server) - Full fake REST API for mock backend

## Author
Mārtiņš Muižnieks

## Acknowledgments
- [Vue.js documentation](https://vuejs.org/v2/guide/)
- [json-server documentation](https://github.com/typicode/json-server)
