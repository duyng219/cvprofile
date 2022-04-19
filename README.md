# cvprofile

-- Deploy GitHub --

Push Project up Github
### `git init, git add ., git commit,....`

Install the package gh-pages into the project
### `npm i gh-pages --save-dev`

Check `package.json` to make sure the package is installed

In the scripts section in `package.json`

Let's add two options:
###`"predeploy": "react-scripts build"` 

and 

###`"deploy": "gh-pages -d build"`

For example: 
`"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "predeploy": "react-scripts build",  
    "deploy": "gh-pages -d build"
  },`

Create `.env` file at the root of the Project

Add `PUBLIC_URL="."` into the file `.env`

Finally, use the command `npm run deploy` to deploy the React app to the Github page

At the repository, go to Setting -> Pages
You will see the link of the website
