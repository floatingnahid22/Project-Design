## Project-Design

# Install yarn:<br>

<p>Yarn is a JavaScript package manager created by Facebook. Yarn stands for Yet Another Resource Negotiator. It provides similar functionalities as NPM. It is an alternative to NPM when installing, uninstalling, and managing package dependencies from the NPM registry or GitHub repositories. yarn install is used to install all dependencies for a project. This is most commonly used when you have just checked out code for a project, or when another developer on the project has added a new dependency that you need to pick up.</p>

```sh
npm install -g yarn
```

# Then run these commands for style and formating:<br>

<p>Prettier takes care of your code formatting, ESLint takes care of your code style. The former does everything automatically for you. If you have set up Prettier, you can configure it to format your file on saving it</p>

```sh
yarn add -D eslint prettier
```

```sh
npx install-peerdeps --dev eslint-config-airbnb-base
```

```sh
yarn add -D eslint-config-prettier eslint-plugin-prettier
```

# After that install nodemon: <br>

<p>It acts as a utility library for keeping track of server changes and automatically restarts our app for us.</p>

```sh
npm i --save-dev nodemon
```

# Then use these below codes:

<p>in your project folder create a new folder called ".vscode" and inside this folder create a file called settings.json. After that copy and paste these below code.</p>
<p>settings.json:</p>

```sh
    {
    "editor.formatOnSave": true,
    "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
    }
```

<p>in your project folder create a file called .eslintrc.json. After that copy and paste these below code.</p>
<p>s.eslintrc.json:</p>

    ```sh
    {
    "extends": ["prettier", "airbnb-base"],
    "parserOptions": {
    "ecmaVersion": 12
    },
    "env": {
    "commonjs": true,
    "node": true
    },
    "rules": {
    "no-console": 0,
    "indent": 0,
    "linebreak-style": 0,
    "prettier/prettier": [
    "error",
    {
    "trailingComma": "es5",
    "singleQuote": true,
    "printWidth": 100,
    "tabWidth": 4,
    "semi": true
    }
    ]
    },
    "plugins": ["prettier"]
    }

````

<p>Copy this script in your projects package.json file</p>
<p>package.json:</p>

```sh
    scripts": {
    "start": "NODE_ENV=development nodemon app.js",
    },
````
