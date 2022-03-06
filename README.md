### Installation:
```shell
npm install eslint --save-dev
```
_Generate configuration file_

```shell
npm init @eslint/config
```
_Run on any file_
```shell
npx eslint myfile.js
```

### Configuration File
eslintrc.{js, yml, json}
```json
{
    "extends": "eslint:recommended",
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["error", "double"]
    }
}
```
> Available Rules: **off**, **warn**, and **error**
#### Specifying globals
```json
{
    "globals": {
        "var1": "writable",
        "var2": "readonly"
    }
}
```
> **writable** equivalent to **true** and **readonly** or **readable** equivalent to **false**

#### Environments
```json
{
    "env": {
        "browser": true,
        "node": true,
        "es6": true
    },
    "globals": {
        "Promise": "off"
    }
}
```
#### Specifying Parser Options
```json
{
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "rules": {
        "semi": "error"
    }
}
```

## Command Line Interface
> npx eslint [options] [file|dir|glob]
```shell
# Run on two files
npx eslint file1.js file2.js

# Run on multiple files
npx eslint lib/**
```
> Available [**options**](https://eslint.org/docs/user-guide/command-line-interface#options)
### Ignoring files from linting
> ESling supports `.eslintignore`
```ignorelang
temp.js
**/vendor/*.js
```
> Integration [guide](https://eslint.org/docs/user-guide/integrations)

> Working with [Rules](https://eslint.org/docs/developer-guide/working-with-rules)

> Contribution [guide](https://eslint.org/docs/developer-guide/contributing)

_Official documentation available [here](https://eslint.org/docs/user-guide/getting-started):_