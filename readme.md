### 1. Prettier

* Install `npm install -D prettier`
* Create `.prettierrc` with empty object
* Update package.json >> script with `"format": "prettier --write \"src/**/*.{js, jsx}\""`
* Test using `npm run format`

### 2. ESLint

* Install `npm install -D eslint@7.18.0 eslint-config-prettier@8.1.0`
* Create .eslintrc.json with `"lint": "eslint \"src/**/*.{js, jsx}\" --quiet"`
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
* Update package.json >> script with ``



