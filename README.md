# To configure ESLINT and PRETTIER in react

Why linting your code is important?

Linting will checks out the code without executing it.

The best part of a linter is finding potential errors in your code that don’t look like them.

## ESLint

Example:

### `// ❌ Oops, what is multiple?
const output = multiple(1, 2);`

ESLint wouldn’t know what add refers to and would throw an error at you. You need to explicitly declare add to correct it:

### `// ✅ Correct
function multiple() {}
const output = multiple(1, 2);`


## 1.Install Eslint Globally

### `npm i -g eslint`

## 2. Initiate Eslint in your project:


### `eslint --init`
(answer the questions)
**NOTE: Use it with caution, It’s very bad idea to disable ESLint every time it spots errors.**

## 3. Confirm installation of eslint-plugin-react


## 4. Look in to .eslintrc.json in root folder , it would contain similar code like below
### ` {
    "env": {
        "browser": true,
        "es6": true
    },
    "extends": [
        "plugin:react/recommended",
        "google"
    ],
    "parserOptions": {
        "ecmaFeatures": {
            "jsx": true
        },
        "ecmaVersion": 2018,
        "sourceType": "module"
    },
    "plugins": [
        "react"
    ],
    "rules": {
    }
} `

## 5. Install prettier dependencies:
### ` npm i -D eslint-config-prettier eslint-plugin-prettier prettier`


`{
    "env": {
        "browser": true,
        "es6": true
    },
    "extends": [
        "plugin:react/recommended",
        "google"
    ],
    "parserOptions": {
        "ecmaFeatures": {
            "jsx": true
        },
        "ecmaVersion": 2018,
        "sourceType": "module"
    },
    "plugins": [
        "react"
    ],
    "rules": {
        "prettier/prettier": [
            "error",
            {
                "printWidth": 80,
                "trailingComma": "es5",
                "semi": false,
                "jsxSingleQuote": true,
                "singleQuote": true,
                "useTabs": true
            }
        ]
    }
}
`


### links 
`https://dev.to/suprabhasupi/learn-to-configure-eslint-and-prettier-in-react-4gp0`
`https://dev.to/swyx/how-to-add-prettier-and-eslint-automation-to-a-react-codebase-2gk1`