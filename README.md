Micro Frontend with Module Federation
This repository serves as a demonstration of using Module Federation to implement a Micro Frontend architecture. Module Federation is a powerful feature introduced in Webpack 5 that enables the creation of scalable and loosely coupled front-end applications by sharing code between different projects at runtime.

Table of Contents
Overview
Getting Started
Project Structure
Usage
Contributing
License
Overview
Micro Frontend is an architectural style that decomposes a large monolithic front-end application into smaller, self-contained, and independently deployable applications known as micro frontends. Each micro frontend is responsible for a specific functionality or business domain.

Module Federation allows us to dynamically load and share code between these micro frontends. It enables us to create a federated architecture where each micro frontend can be developed and deployed independently while still working seamlessly together.

This repository demonstrates a simple example of a micro frontend setup using Module Federation. It consists of two micro frontends, app-shell and feature-module, which are hosted and integrated into a single application.

Getting Started
To get started with this project, follow these steps:

Clone the repository:
bash
Copy code
git clone https://github.com/TranBinh2311/micro_front_end.git
Install the dependencies for both the app-shell and feature-module:

Start the development servers for both micro frontends:
bash

cd container
npm install

cd cart
npm install

cd products
npm install


Open your browser and visit http://localhost:8080 to see the application running.
Project Structure
The project structure is organized as follows:

java
Copy code
micro_front_end/
  |- cart/
  |    |- src/
  |    |- package.json
  |
  |- container/
  |    |- src/
  |    |- package.json
  |
  |- products/
  |    |- src/
  |    |- package.json
  |- README.md
The app-shell directory contains the code for the main application shell or container, which integrates and orchestrates the micro frontends.
The feature-module directory contains the code for a specific feature or micro frontend that will be loaded dynamically by the app shell.
Usage
In this example, the app-shell consumes and integrates the feature-module using Module Federation. The app-shell dynamically loads and renders the feature-module when a specific route is accessed or a user action triggers its loading.

To see it in action, follow the Getting Started instructions mentioned above, and open http://localhost:8080 in your browser. You should see the main application shell with the integrated feature-module.

Feel free to explore the code of both the app-shell and feature-module to understand how they are implemented and how Module Federation is used to share and load code between them.

Contributing
Contributions are welcome! If you find any issues or want to enhance this repository, please feel free to open an issue or submit a pull request.

License
This repository is licensed under the MIT License. You are free to use, modify, and distribute this code as per the terms of the license.