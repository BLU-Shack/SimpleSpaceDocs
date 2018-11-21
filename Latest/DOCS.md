# Global





* * *

## Class: Client



## Class: Client


**options**: `ClientOptions` , The Client Options.
**bots**: `Store.&lt;string, Bot&gt;` , Cached bots that are listed on the site, mapped through bot IDs.
**emojis**: `Store.&lt;string, Emoji&gt;` , Cached emojis that are listed on the site, mapped through emoji IDs.
**guilds**: `Store.&lt;string, Guild&gt;` , Cached guilds that are listed on the site, mapped through guild IDs.
**readyAt**: `Date` , Date when Client was initially ready.
**readyTimestamp**: `number` , The timestamp when Client was initially ready.
**endpoint**: `string` , The endpoint URL, used to interact with the site.
### Client.isObject(obj) 

Checks whether or not a given item is an object.

**Parameters**

**obj**: `object`, The item to testify against.

**Returns**: `boolean`, Whether or not the item that is testifyed is an object.

### Client.edit(options, preset) 

Edit at least one or more key-value pair in the instance.

**Parameters**

**options**: `ClientOptions`, A thing.

**preset**: `boolean`, Whether or not to have preset rules when setting values.

**Returns**: `ClientOptions`, The new client options.

**Example**:
```js
console.log(Client.edit({ log: false }).options);
```

### Client.fetchAllBots(options) 

Returns all bots on the site.

**Parameters**

**options**: `FetchOptions`, Fetch Options.

**Returns**: `Promise.&lt;Array.&lt;Bot&gt;&gt;`, All bots on the site.

### Client.fetchAllGuilds(options) 

Fetches all guilds on the site.

**Parameters**

**options**: `FetchOptions`, Fetch Options

**Returns**: `Promise.&lt;Array.&lt;Guild&gt;&gt;`, All guilds on the site.

### Client.fetchAllEmojis(options) 

Fetch all emojis listed on the site.

**Parameters**

**options**: `FetchOptions`, Fetch Options.

**Returns**: `Promise.&lt;Array.&lt;Emoji&gt;&gt;`, All emojis on the site.

### Client.fetchBot(botID, options) 

Fetch a bot from the site.

**Parameters**

**botID**: `string`, The bot ID to fetch from the list.

**options**: `FetchOptions`, FetchOptions.

**Returns**: `Promise.&lt;Bot&gt;`, Returns the bot contents/specified item.

**Example**:
```js
Client.fetchBot('463803888072523797', { specified: 'username' })
 .then(username => console.log(username))
 .catch(console.log);
```

### Client.fetchEmoji(emojiID, options) 

Fetch an emoji listed on the site.

**Parameters**

**emojiID**: `string`, The emoji ID to fetch.

**options**: `FetchOptions`, Fetch Options.

**Returns**: `Promise.&lt;Emoji&gt;`, Returns the emoji contents/specified item.

### Client.fetchGuild(guildID, options) 

Fetch a guild on the list.

**Parameters**

**guildID**: `string`, The guild ID to fetch from the list.

**options**: `FetchOptions`, Supply if you want to get a specific value, etc. 'prefix'

**Returns**: `Promise.&lt;Guild&gt;`, Returns the guild contents/specified item.

### Client.fetchGuildEmojis(guildID, options) 

Fetches a guild's emojis.

**Parameters**

**guildID**: `string`, The guild ID to fetch its emojis from.

**options**: `FetchOptions`, Fetch Options.

**Returns**: `Promise.&lt;Array.&lt;Emoji&gt;&gt;`, The array of the guild's emojis.

### Client.fetchSelf(options) 

Fetch a bot using the ID supplied on initialization.

**Parameters**

**options**: `FetchOptions`, Options.

**Returns**: `Promise.&lt;Bot&gt;`, Returns the bot contents/specified item.

### Client.fetchStats(options) 

Fetch the site statistics.

**Parameters**

**options**: `FetchOptions`, Supply if you want a specific value, etc. 'guilds' or 'bots'

**Returns**: `Promise.&lt;Stats&gt;`, Returns site stats/specified value.

### Client.fetchUpvotes(options) 

Fetch users in the last 24 hours who have upvoted your bot.

**Parameters**

**options**: `UpvoteFetchOptions`, Upvote Fetch Options.

**Returns**: `Promise.&lt;Array.&lt;PartialUser&gt;&gt;`, The array of the user objects/user IDs.

**Example**:
```js
Client.fetchUpvotes({ ids: true });
```

### Client.fetchUser(userID, options) 

Fetches a user that had logged on to botlist.space

**Parameters**

**userID**: `string`, The user ID to fetch.

**options**: `FetchOptions`, FetchOptions.

**Returns**: `Promise.&lt;User&gt;`, Returns the user contents/specified item.

### Client.hasUpvoted(userID) 

Checks if a user has upvoted your bot.

**Parameters**

**userID**: `string`, The user ID to check if they have upvoted your bot.

**Returns**: `Promise.&lt;boolean&gt;`, Whether or not the user has upvoted your bot.

### Client.setGuilds(options) 

**Parameters**

**options**: `PostOptions`, Post Options.

 - **options.token**: `string`, The API token for posting.

 - **options.botID**: `string`, The bot ID for posting.

 - **options.guildSize**: `string`, The number (if no shards)/an array of numbers (if shards) to push to the API. Unneeded if a client was supplied.

**Fires**: Client#event:post

**Returns**: `Promise.&lt;object&gt;`, Returns the code, and a message.



* * *










