### React 
`npm install react@17.0.1 react-dom@17.0.1`

### 1. Prettier

* Install `npm install -D prettier`
* Create `.prettierrc` with empty object
* Update package.json >> script with `"format": "prettier --write \"src/**/*.{js, jsx}\""`
* Test using `npm run format`

### 2. ESLint

* Install `npm install -D eslint@7.18.0 eslint-config-prettier@8.1.0`
* Install `npm install -D eslint-plugin-import@2.22.1 eslint-plugin-jsx-a11y@6.4.1 eslint-plugin-react@7.22.0`
* Create .eslintrc.json with below code
```
  {
    "extends": [
      "eslint:recommended",
      "plugin:import/errors",
      "plugin:react/recommended",
      "plugin:jsx-a11y/recommended",
      "plugin:react-hooks/recommended",
      "prettier"
    ],
    "rules": {
      "react/prop-types": 0,
      "react/react-in-jsx-scope": 0
    },
    "plugins": ["react", "import", "jsx-a11y"],
    "parserOptions": {
      "ecmaVersion": 2021,
      "sourceType": "module",
      "ecmaFeatures": {
        "jsx": true
      }
    },
    "env": {
      "es6": true,
      "browser": true,
      "node": true
    },
    "settings": {
      "react" : {
        "version": "detect"
      }
    }
  }
```
* Update package.json >> script with `"lint": "eslint \"src/**/*.{js, jsx}\" --quiet"`

### 3. Git

* Initiate `git init`
* Create .gitignore

```
node_modules/
.cache/
dist/
.env
.DS_Store
coverage/
```

### 4. Parcel

* Install `npm install -D parcel@1.12.3`

### 5. Babel

* Add .babelrc
```
{
  "presets": [
    [
      "@babel/preset-react",
      {
        "runtime": "automatic"
      }
    ]
  ]
}
```
* Install `npm install -D @babel/core@7.12.16 @babel/preset-react@7.12.13`
* Target browsers in package.json

```
  "browserslist": [
    "last 2 Chrome versions"
  ]
```

### 6. ReactRouter

* Install `npm install react-router-dom@5.2.0`

### 7. Jest/testing Library

* Install `npm install -D jest@26.6.3 @testing-library/react@11.2.5 @testing-library/react-hooks@5.1.0`
* * Install `npm install -D react-test-renderer@17.0.1`

```
  {
    "presets": [
      [
        "@babel/preset-react",
        {
          "runtime": "automatic"
        }
      ],
      "@babel/preset-env"
    ],
    "plugins": ["@babel/plugin-proposal-class-properties"],
    "env": {
      "test": {
        "presets": [
          [
            "@babel/preset-env",
            {
              "targets": {
                "node": "current"
              }
            }
          ]
        ]
      }
    }
  }
```

* Update `package.json` scripts
```
  "test": "jest",
  "test:watch": "jest --watch"
```

### 8. React Class Babel (Optional)

* Install `npm i -D @babel/plugin-proposal-class-properties@7.13.0 @babel/preset-env@7.13.5 @babel/eslint-parser@7.13.4`
* Add in `.babelrc` && `.eslintrc.json`
```
{
  "presets": [
    [
      "@babel/preset-react",
      {
        "runtime": "automatic"
      }
    ],
    "@babel/preset-env"
  ],
  "plugins" : [
    "@babel/plugin-proposal-class-properties"
  ]
}
```

```
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "plugin:react-hooks/recommended",
    "prettier"
  ],
  "rules": {
    "react/prop-types": 0,
    "react/react-in-jsx-scope": 0
  },
  "plugins": ["react", "import", "jsx-a11y"],
  "parser": "@babel/eslint-parser",
  "parserOptions": {
    "ecmaVersion": 2021,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  },
  "settings": {
    "react" : {
      "version": "detect"
    }
  }
}
```



