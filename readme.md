# pack-npm

Get a list of Github repositories of specified username sorted by numbers of stars in descending order and last updated time

## Installation

```js
# using npm
npm install pack-npm

# using yarn
yarn add pack-npm
```

## Usage

```js
# using require
const { getRepos } = require('pack-npm');

# using import
import { getRepos } from 'pack-npm';
```

## Example

### Using promises:

```js
getRepos({
  username: 'username', // provide GitHub username here
  page: 1, // optional property: default value is 1
  per_page: 50 // optional property: default value is 30
}).then((repositories) => console.log(repositories));
```

### Using async/await:

```js
const getRepositories = async function () {
  const repositories = await getRepos({
    username: 'username', // provide GitHub username here
    page: 1, // optional property: default value is 1
    per_page: 50 // optional property: default value is 30
  });
  console.log(repositories);
};

getRepositories();
```
