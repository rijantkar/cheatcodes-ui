### React 
`npm install react@17.0.1 react-dom@17.0.1`

### 1. Prettier

* Install `npm install -D prettier`
* Create `.prettierrc` with empty object
* Update package.json >> script with `"format": "prettier --write \"src/**/*.{js, jsx}\""`
* Test using `npm run format`

### 2. ESLint

* Install `npm install -D eslint@7.18.0 eslint-config-prettier@8.1.0`
* Create .eslintrc.json with below code
```
  {
    "extends": ["eslint:recommended", "prettier"],
    "plugins": [],
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



