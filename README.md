# Wide Area Frequency Measurement System (WAFMS) #

## Web Development ##

The web development section of the wide-area frequency measurement project is focused on building an efficient and user-friendly application to monitor and analyze frequency measurements across different locations. 

### This section will encompass three key components:  ###
- Frontend development using ReactJS
- Backend development using Node.js
- Database creation using MySQL

The frontend section will involve creating dynamic and responsive user interfaces to visualize real-time frequency data and location-based insights. In the backend section, we will establish a robust Node.js server to handle data requests, process business logic, and interact with the MySQL database. Throughout the development process, we will follow steps including project setup, designing and implementing the frontend, defining the database schema, establishing database connectivity, implementing API endpoints for data retrieval and updates, error handling, testing, and finally, deploying the application to ensure a seamless user experience and accurate frequency measurement analysis.

### Software tools required ###
- Visual Studio Code
- MySQL Workbench 
- NodeJS

### Visual Studio Code download ###

To download the latest version of VS Code click <u>[here](https://code.visualstudio.com/)</u> for the respective OS and for the download tutorial, you can refer to this <u>[link](https://www.youtube.com/watch?v=u8APxuCICkA)</u>. 
To set up vs code install the necessary extensions mentioned <u>[here](https://www.syncfusion.com/blogs/post/top-15-vs-code-extensions-every-developer-should-know.aspx)</u>. To do so click on ![Image2](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/Extension.png) this.

### MySQL Workbench download ###

To download the latest version of MySQL workbench click <u>[here](https://www.mysql.com/downloads/)</u> 
Downloads --> MySQL Community (GPA) Downloads -->  MySQL Installer for Windows --> **mysql-installer-community-8.0.34.0.msi** (version may vary, and do not download mysql-installer-web-community-8.0.34.0.msi instead of mentioned above .msi file)
For the download tutorial, refer to this <u>[link](https://www.youtube.com/watch?v=VK4nTHqbcMg)</u>. Once you download it successfully open the command prompt and run the command **mysql --version** to ensure successful installation of MySQL workbench, it will show the version of MySQL. Make sure that a path is added to **System Environment Variable**.
Required extension on VS Code mentioned <u>[here](https://www.syncfusion.com/blogs/post/7-vs-code-extensions-for-react-developers.aspx).</u>

### NodeJS download ###

To download the latest version of **Node.js** click <u>[here](https://nodejs.org/en)</u>. For a download tutorial, you can also refer to this <u>[link](https://www.youtube.com/watch?v=06X51c6WHsQ)</u>. Make sure that path is added to **System Environment Variable**.

Required Extensions: 

- npm
- npm Intellisense
- ESLint

## Database Creation (MySQL) ##

The initial view of the MySQL workbench is as below:

![workbech](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/MySQL%20WorkBench.png)

Users can create as many local instances by clicking on plus sign as shown in the above window.

There are two ways to create tables in a database:

**Method 1: Using MySQL Workbench UI**

1. **Open MySQL Workbench:** Launch MySQL Workbench, when you open this window for the first time, on clicking on the local instance you have to enter your username (i.e. usually **root** and password).
2. **Create a New Database:** Once connected, you'll see the available databases listed under the "SCHEMAS" section in the left sidebar. Right-click on the "SCHEMAS" and select "Create Schema..." or click on the "Create a new schema in the connected server" [icon](https://www.google.com/url?sa=i&url=https%3A%2F%2Fgkscientist.com%2Fcreate-database-in-mysql%2F&psig=AOvVaw2I-bLYfXr-h_y03njZ1Wye&ust=1691402828899000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCJDQ0uDkx4ADFQAAAAAdAAAAABAP) icon (blue cylinder with a + symbol).
3. **Name the New Database:** A dialog box will appear where you can enter the name of the new database. Provide a name and click "Apply" to create the database.
4. **Select the New Database:** The newly created database will now appear under the "SCHEMAS" section. Double-click on the database name to select it as the current database.
5. **Create Tables:** With the new database selected, go to the "Table" tab in the main window and click on the "Create Table" button (sheet of paper with a + symbol). This will open a new window where you can define the table's columns, data types, and constraints.

Fill in the necessary details and click "Apply" to create the table.

Method 2: Using SQL Query

1. Open MySQL Workbench: Connect to your MySQL server as explained in Method 1.
2. Open SQL Editor: Click on the "SQL Editor" button in the top toolbar. This will open a new tab for writing and executing SQL queries.
3. Create Database: To create a new database using an SQL query, you can use the CREATE DATABASE statement:

## Backend Development and Database Connectivity (Node.js) ##



## Frontend Development & Full Stack Integration (React.js) ##
For the frontend we used React.js. React is a free and open-source front-end JavaScript library for building user interfaces based on components. It is maintained by Meta and a community of individual developers and companies. React can be used to develop single-page, mobile, or server-rendered applications with frameworks like Next.js.

To create a new React app, follow these steps:

1. **Install Node.js and npm:** Ensure you have Node.js (which includes npm, the Node Package Manager) installed on your computer.
2. **Create a New React App:** Open your terminal or command prompt and run the following commands in the same order to create a new React app using Create React App (a popular tool to set up a new React project):

Firstly, check <u> [this](https://www.npmjs.com/package/create-react-app) </u> wesite for the latest version. This package includes the global command for Create React App.

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
- public: This folder includes the public assets like index.html and other static files.
- src/index.js: This is the entry point of your React app where you can find the rendering of the React components into the DOM.

![ReactApp](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/ReactApp.png)

Now you are free to modify the design of the website as per your requirement. Like shown below, create two separate files for Components and Pages. Here, each component name (AppHeader, AppRoutes, PageContent, SideMenu) depicts its purpose. A **pages** file contains the number of web pages that we want on our website.

![Image4](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/explorer1.png) ![Image5](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/explorer2.png) ![Image6](https://github.com/rinapachkale/WAFMS-Project-Blueprint/blob/master/explorer3.png)

The link below provides a vast collection of node packages

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

That's it! You have now successfully created a new frontend using React. Happy coding!
