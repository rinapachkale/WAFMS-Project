# Wide Area Frequency Measurement System (WAFMS) #

## Full Stack Web Development ##

The web development section of the wide-area frequency measurement project is focused on building an efficient and user-friendly application to monitor and analyze frequency measurements across different locations. 

### This section will encompass three key components:  ###
- Frontend development using ReactJS
- Backend development using Node.js
- Database creation using MySQL

The frontend section will involve creating dynamic and responsive user interfaces to visualize real-time frequency data and location-based insights. In the backend section, we will establish a robust Node.js server to handle data requests, process business logic, and interact with the MySQL database. Throughout the development process, we will follow steps including project setup, designing and implementing the frontend, defining the database schema, establishing database connectivity, implementing API endpoints for data retrieval and updates, error handling, testing.

### Software tools required ###
- Visual Studio Code
- MySQL Workbench 
- NodeJS

### Visual Studio Code download ###

To download the latest version of VS Code click <u>[here](https://code.visualstudio.com/)</u> for the respective OS and for the download tutorial, you can refer to this <u>[link](https://www.youtube.com/watch?v=u8APxuCICkA)</u>. 
To set up vs code install the necessary extensions mentioned <u>[here](https://www.syncfusion.com/blogs/post/top-15-vs-code-extensions-every-developer-should-know.aspx)</u>. To do so click on ![Image2](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/Extension.png) icon.

### MySQL Workbench download ###

To download the latest version of MySQL workbench click <u>[here](https://www.mysql.com/downloads/).</u> 

Downloads --> MySQL Community (GPA) Downloads -->  MySQL Installer for Windows --> **mysql-installer-community-8.0.34.0.msi** (version may vary, and do not download mysql-installer-web-community-8.0.34.0.msi instead of mentioned above .msi file)

For the download tutorial, refer to this <u>[link](https://www.youtube.com/watch?v=VK4nTHqbcMg)</u>. Once you download it successfully open the command prompt and run the following command to ensure successful installation of MySQL workbench, it will show the version of MySQL on your device. 

**`mysql --version`**

Make sure that a path is added to **System Environment Variable**. You can refer to this [Link](https://www.youtube.com/watch?v=a1AMVA9p3W0) for how to add path to system environment variables.

### NodeJS download ###

To download the latest version of **Node.js** click <u>[here](https://nodejs.org/en)</u>. For a download tutorial, you can also refer to this <u>[link](https://www.youtube.com/watch?v=06X51c6WHsQ)</u>. Make sure that path is added to **System Environment Variable**.

Required Extensions on VS Code: 

- npm
- npm Intellisense
- ESLint

## Database Creation (MySQL) ##

The initial view of the MySQL workbench is as below:

![workbech](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/MySQL%20WorkBench.png)

Users can create as many local instances by clicking on plus sign as shown in the above window. If your are stuck anywhere, refer to this tutorial video, <u>[click here](https://www.youtube.com/watch?v=wALCw0F8e9M&t=196s)</u>

There are two ways to create tables in a database:

### Method 1: Using MySQL Workbench UI ###

1. **Open MySQL Workbench:** Launch MySQL Workbench, when you open this window for the first time, on clicking on the local instance you have to enter your username (i.e. usually **root**) and password.
2. **Create a New Database:** Once connected, you'll see the available databases listed under the "SCHEMAS" section in the left sidebar. Right-click on the "SCHEMAS" and select "Create Schema..." or click on "Create a new schema in the connected server" icon.

![icon](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/icon.png)

3. **Name the New Database:** A dialog box will appear where you can enter the name of the new database. Provide a name and click "Apply" to create the database.

![db](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/db_creation.png)

4. **Select the New Database:** The newly created database will now appear under the "SCHEMAS" section. Double-click on the database name to select it as the current database.
5. **Create Tables:** With the new database selected, go to the "Table" tab in the main window and click on the "Create Table" button.

![dt](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/create%20table.webp)

This will open a new window where you can define the table's columns, data types, and constraints.

![apply](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/table%20dt.png)

Fill in the necessary details and click "Apply" to create the table.

### Method 2: Using SQL Query ###

1. **Open MySQL Workbench.**
2. **Open SQL Editor:** Click on the "SQL Editor" button in the top toolbar. This will open a new tab for writing and executing SQL queries.
3. **Create Database:** To create a new database using an SQL query, you can use the CREATE DATABASE statement:
 
**`CREATE DATABASE database_name;`**

4. **Create Table:** Write a query to create a table. E.g.

**CREATE TABLE `esp_database_php`.`esp_data_php` (**

  **`id` INT(6) UNSIGNED NOT NULL AUTO_INCREMENT,**
  
  **`sensor` VARCHAR(30) CHARACTER SET 'utf8mb4' NOT NULL,**
  
  **`location` VARCHAR(30) CHARACTER SET 'utf8mb4' NOT NULL,**
  
  **`value1` VARCHAR(30) CHARACTER SET 'utf8mb4' NULL DEFAULT NULL,**
  
  **`value2` VARCHAR(30) CHARACTER SET 'utf8mb4' NULL DEFAULT NULL,**
  
  **`value3` VARCHAR(30) CHARACTER SET 'utf8mb4' NULL DEFAULT NULL,**
  
  **`reading_time` TIMESTAMP(4) NOT NULL DEFAULT current_timestamp(),**
  
  **PRIMARY KEY (`id`));**

With both methods, you can now create databases and tables in MySQL Workbench according to your requirements. Choose the method that suits your preference and the complexity of your project.


## Backend Development and Database Connectivity (Node.js) ##

Firstly, create node application by following steps:

1. Create empty folder in your PC (preferably in C drive) and open it in command prompt. Now give following command:

**`npm init`** and add package name, author and keep pressing **ENTER** button till it reaches to this note **`Is this OK? (yes)`**. Type **yes** there and press **ENTER**. Now it will exit the current command scope.

![img1](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/npm%20init.png)

![img2](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/backend1.png)

Now install the required packages (express, mysql):

**`npm i express --save`**

**`npm i mysql --save`**

![img3](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/express%20mysql.png)

Now open this project folder in VS Code. Add two more files **index.js** (for API creation) and **database.js** (for database connectivity). Once your project file is ready to run, open terminal window of VS Code and use following command to run the project:

**`node index.js`** 

After running the file, the server will be up and running at the specified port, and it will be ready to handle incoming requests. Now, go to the browser and type the URL of your server (e.g. http://localhost:3004/). When a client sends a GET request to the root path ('/'), the server will respond with the data fetched from the respective table in the database.


## Frontend Development & Full Stack Integration (React.js) ##
For the frontend we used React.js. React is a free and open-source front-end JavaScript library for building user interfaces based on components. It is maintained by Meta and a community of individual developers and companies. React can be used to develop single-page, mobile, or server-rendered applications with frameworks like Next.js.

To create a new React app, follow these steps:

1. **Install Node.js and npm:** Ensure you have Node.js (which includes npm, the Node Package Manager) installed on your computer.
2. **Create a New React App:** Open your terminal or command prompt and run the following commands in the same order to create a new React app using **Create React App tool** (a popular tool to set up a new React project):

Firstly, check <u> [this](https://www.npmjs.com/package/create-react-app) </u> website for the latest version of above-mentioned tool. This package includes the global command for Create React App.

**`npm i -g create-react-app@1.5.2`** 

It should give results like the below:

![Image](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/create-react-app.png)

Then,

**`create-react-app my-react-app`**

It should give results like the below:

![Image2](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/my-react-app.png)

![Image3](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/my-react-app1.png)

Replace my-react-app with the desired name of your project. This command will generate a new folder with the project structure and necessary files and this might take some time. Once the project is created then open this project in VS Code (File -> Open folder).

![Image3](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/VS%20Code%20window.png)

Now, one can only modify the **src file**. In the project directory, start the development server by running the command **npm start** in the terminal window of **VS Code**, this will launch the app in your default web browser at http://localhost:3000, and it will automatically update as you make changes.

You'll find the basic structure of a React app inside the project folder. Key folders and files include:

- src: This folder contains the main source code of your React application.
- public: This folder includes public assets like index.html and other static files.
- src/index.js: This is the entry point of your React app where you can find the rendering of the React components into the DOM.

![ReactApp](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/ReactApp.png)

Now you are free to modify the design of the website as per your requirement.
The link below provides a vast collection of node packages:

[https://www.npmjs.com/](https://www.npmjs.com/)

**Other useful packages of components and design patterns are:**

1. **Ant Design:** Its main purpose is to provide developers with a set of high-quality, efficient, and customizable UI components and design patterns for building modern web applications.

Link: [https://ant.design/](https://ant.design/)

2. **Recharts:** Recharts is a popular open-source JavaScript charting library specifically designed for React, making it an excellent choice for developers building data-driven web applications.

Link: [https://recharts.org/en-US/api](https://recharts.org/en-US/api)

3. **Chart.js:**  Chart.js provides developers with a simple and flexible JavaScript library for creating interactive and visually appealing charts and data visualizations on web pages. Chart.js is an open-source library that allows developers to easily integrate various types of charts into their web applications without the need for complex configurations.

Link: [https://www.chartjs.org/docs/latest/](https://www.chartjs.org/docs/latest/)

4. **React-Bootstrap:** React-Bootstrap is a library that combines the power and flexibility of React with the popular Bootstrap framework, making it easier for developers to create visually appealing and mobile-friendly user interfaces.

Link: [https://react-bootstrap.netlify.app/docs/getting-started/introduction](https://react-bootstrap.netlify.app/docs/getting-started/introduction)

For website architecture, you can refer to this video [link](https://www.youtube.com/watch?v=xvBUgdKUz5g&t=2083s) and you can take the help of chatGPT too.

### Full stack integration ###

Create a JavaScript function (refer to the code) that fetches data from a backend server and performs some data manipulation before setting the data into the component's state using setHistorianData. It is essential in full-stack integration for the following reasons:

**Data Retrieval:** The fetchData function is responsible for fetching data from the backend server. In full-stack integration, the frontend (React component in this case) communicates with the backend server to obtain data from a database or perform certain operations on the server side.

**Asynchronous Operations:** The function uses async/await, which is crucial when making asynchronous API calls. It ensures that the function waits for the response from the server before proceeding further. Asynchronous operations are common in full-stack applications as they allow the front end to efficiently interact with the backend without blocking the user interface.

**Data Transformation:** The fetched data may require transformation before being used in the front end. In this code, the timestamp from the fetched data is converted into human-readable date and time formats. This data transformation allows the front end to present the data in a more user-friendly manner.

**State Management:** The converted data is set into the component's state using setHistorianData. State management is a critical aspect of frontend development, and it allows React components to maintain and update their internal state, enabling dynamic and responsive user interfaces.

**Full-stack Communication:** The code demonstrates the communication and data exchange between the frontend (React) and the backend (Node.js in this case). This is a fundamental aspect of full-stack integration, as it enables seamless interaction between different layers of the application.

**Error Handling:** The code includes error handling using try/catch to handle any errors that may occur during the data fetching process. Proper error handling is essential in full-stack integration to ensure that the application gracefully handles unexpected situations and provides meaningful feedback to the user.

That's it! You have now successfully created a full-stack Web application using Reactjs, Nodejs, and MySQL. Happy coding!
