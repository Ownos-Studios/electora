# electora

### About the project
This project shababa

### Tech specs
- JavaScript
- HTML
- CSS
- EJS template engine
- Node JS
- Express JS
- Mongoose

## Environment Setup

- Drop a :star: on the GitHub repository.
- Download [Node Js and npm(Node package manager)](https://nodejs.org/en/) (when you download Node, npm also gets installed by default)
- Mongo DB community editition is free and a great software in order to work with MongoDB applications. [Download Mongo DB community editition](https://docs.mongodb.com/manual/administration/install-community/)
- Robo 3T is a desktop graphical user interface (GUI) for Mongo DB. It can help to skip running all the Mongo DB commands manually every time we want to access the data. [Download Robo 3T](https://robomongo.org/download) **(optional)**


- Clone the repository by running command
```
git clone https://github.com/ <your user-name> /electora.git
```
in your git bash.

- Run command `cd electora`.

- Run this command to install all dependencies for the project.
```
npm install
```

- Run this command on your terminal/ bash to start the Mongo server on port 27017(default).
```
mongod
```

- Run this command to start the project on local host 3000.
```
node app
```

- Open link to view the website in your browser window if it doesn't open automatically.
```
http://localhost:3000/
```

- You can learn more about EJS template engine and its syntax to know how we can use it inside our HTML using the [documentation](https://ejs.co/#docs)

#### Some useful Mongo DB commands if you are using the terminal instead of the GUI-
```
show dbs
use db <db name>
show collections
<db name> .find()
```

------

### Development
- The project follows an engineered structure for both backend and frontend development. The initial entry point is by default ```index.js```
- Each directory has a ```package.json``` file, which is primarily to make importing various files easy throughout the app.
- The project utilises ```SCSS``` for custom styling purposes and Bootstrap (v4.3) for it's primary styling purposes.
- The project contains the following scripts:
    - ```npm run dev```: This script runs the app in development mode. The app is run on the nodemon package for this.
    - ```npm start```: This script runs the app with the ```node``` command.

    #### Guidelines
    - Each module has a particular directory named after it, which contains the route files for the same. Example: authentication module has a directory named ```authentication/``` which contains ```login.js``` and ```signup.js```
    - The usage of each directory is listed below for ease of navigation and understanding.

    #### ```docs/```
    - This directory contains all the documentation necessary to understand the project to its full capacity, covering the very basics to the very advanced features, both in brief and detail.
    
    #### ```routes/```
    - This directory contains all the routes for ```get``` and ```post``` methods.

    #### ```models/```
    - This directory contains all the Mongoose models and schemas.

    #### ```controllers/```
    - This directory contains all the functions executed at a particular route.
    
    #### ```views/```
    - This directory contains all the EJS pages of the app.
    - ```head.ejs```: This file contains all the common tags and meta information for a webpage.
    - ```scripts.ejs```: This file contains all the common scripts for a webpage.

    #### ```public/```
    - This directory contains all the miscellaneous scripts and stylesheets which are used in the front-end. These scripts are commonly used all across the app.
    - ```css/_vars.scss```: This file contains all the color and font variables that are used in the app.
    - ```css/_common.scss```: This file contains all the common SCSS properties that are used throughout the app.
    - ```js/helper.js```: This file contains a class named ```Helper``` which contains several miscellaneous functions used repeatedly in the app. Import and use the class by the following way: 
    ```
    import Helper from 'misc/helper'
    const helper = new Helper()
    ```
        - ```helper.parseTime(x)```: Returns a string in the format of DD/MM/YYYY 00:00 (IST) for any epoch timestamp passed as the variable ```x```
        - ```helper.reduceString(string, threshold)```: Returns a string which is trimmed down to a particular ```threshold``` of words. Example, if ```threshold``` is passed as ```50```, the ```string``` that is passed into the function will be cut down to 50 words. If ```string``` is less than 50 words in length, it will return the string as it is.
