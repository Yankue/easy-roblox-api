# easy-roblox-api
This package is an extremely easy package, to easily get data 
from the Roblox API.
## Installation
Install with NPM:
```
$ npm install easy-roblox-api
```
### Version
The current version is v2.0.0 - which added the `getGroup()` function. This is the most stable and recommended version.

## Quick Start
### Information about a User
This will get a lot of data about user:
```js
const roblox = require('easy-roblox-api');
roblox.getUser("Some rbx username", "username").then(response => {
   console.log(response); 
}).catch(() => {
  console.log("An error occured, most likely that user does't exist!");
});

/* This will log something like this:
{
  id: 1,
  username: 'John Doe',
  description: 'The users description here',
  status: 'The users status here',
  created: '2016-07-04T16:59:11.313Z',
  avatar_url: 'URL to an image of the user's avatar',
  friends: {
    count: 8,
    ids: [array-of-friends-ids]
  },
  followers: {
    count: 14,
    ids: [array-of-followers-ids]
  },
  following: {
    count: 69,
    ids: [array-of-followings-ids]
  }
}*/
```
As an alternative, you can get user information using an ID:
```js
const roblox = require('easy-roblox-api');
roblox.getUser("140445252", "id").then(response => {
   console.log(response); 
});
```
If you leave the 2nd parameter of `getUser` empty, it will assume it is an ID.

### Information about a Group

```js
roblox.getGroup("some group", "name").then(res => {
    console.log(res);
}).catch(console.error);

/* This will log something like this:
{
  id: 1,
  name: 'Example name',
  description: 'Example group description',
  owner: { id: 4, username: 'John Doe' },
  membercount: undefined,
  thumbnail: 'some-url-to-a-png',
  shout: {
    content: 'omghi',
    created: '2021-03-11T19:09:57.3352677Z',
    author: { id: 4, username: 'John Doe' }
  },
  roles: [
    { id: 7, name: 'Some role name', membercount: 0 },
    { id: 69, name: 'Some other role name', membercount: 6 }
  ]
}
*/
```
Just like when getting user data, you can put `id` instead of `name` as parameter 2 when getting group data. ID is the default if none is provided.


## Support
To get support using the package, report bugs, request updates, or any other sort of request, please use our [GitHub issues page](https://github.com/Yankue/easy-roblox-api/issues), where I will gladly help you.

## Documentation
Documentation will be on the wiki on GitHub, but this is coming soon.
