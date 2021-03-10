# easy-roblox-api
This package is an extremely easy package, to easily get data 
from the Roblox API.
## Installation
Install with NPM:
```
$ npm install easy-roblox-api
```

## Quick Start
This will get a lot of data about user:
```js
const roblox = require('easy-roblox-api');
roblox.getUser("Yankue", "username").then(response => {
   console.log(response); 
});

/* This will log something like this:
{
  id: 140445252,
  username: 'Yankue',
  description: 'The users description here',
  status: 'The users status here',
  created: '2016-07-04T16:59:11.313Z',
  avatar_url: 'URL to an image of the user's avatar',
  friends: {
    count: 16,
    ids: [array-of-friends-ids]
  },
  followers: {
    count: 10,
    ids: [array-of-followers-ids]
  },
  following: {
    count: [],
    ids: [array-of-followings-ids]
  }
}*/
```

## Documentation
