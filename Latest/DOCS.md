## Client
Main client class for interacting to botlist.space

**Kind**: global class

* [Client](#Client)
    * [new Client([options])](#new_Client_new)
    * _instance_
        * [.options](#Client+options) : <code>ClientOptions</code>
        * [.bots](#Client+bots) : <code>Store.&lt;string, Bot&gt;</code>
        * [.emojis](#Client+emojis) : <code>Store.&lt;string, Emoji&gt;</code>
        * [.guilds](#Client+guilds) : <code>Store.&lt;string, Guild&gt;</code>
        * [.readyAt](#Client+readyAt) : <code>Date</code>
        * [.readyTimestamp](#Client+readyTimestamp) : <code>number</code>
        * [.edit([options], [preset])](#Client+edit) ⇒ <code>ClientOptions</code>
        * [.fetchAllBots(options)](#Client+fetchAllBots) ⇒ <code>Promise.&lt;Array.&lt;Bot&gt;&gt;</code>
        * [.fetchAllGuilds(options)](#Client+fetchAllGuilds) ⇒ <code>Promise.&lt;Array.&lt;Guild&gt;&gt;</code>
        * [.fetchAllEmojis(options)](#Client+fetchAllEmojis) ⇒ <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code>
        * [.fetchBot(botID, [options])](#Client+fetchBot) ⇒ <code>Promise.&lt;Bot&gt;</code>
        * [.fetchEmoji(emojiID, options)](#Client+fetchEmoji) ⇒ <code>Promise.&lt;Emoji&gt;</code>
        * [.fetchGuild(guildID, [options])](#Client+fetchGuild) ⇒ <code>Promise.&lt;Guild&gt;</code>
        * [.fetchGuildEmojis(guildID, options)](#Client+fetchGuildEmojis) ⇒ <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code>
        * [.fetchSelf([options])](#Client+fetchSelf) ⇒ <code>Promise.&lt;Bot&gt;</code>
        * [.fetchStats([options])](#Client+fetchStats) ⇒ <code>Promise.&lt;Stats&gt;</code>
        * [.fetchUpvotes([options])](#Client+fetchUpvotes) ⇒ <code>Promise.&lt;Array.&lt;PartialUser&gt;&gt;</code>
        * [.fetchUser(userID, [options])](#Client+fetchUser) ⇒ <code>Promise.&lt;User&gt;</code>
        * [.hasUpvoted(userID)](#Client+hasUpvoted) ⇒ <code>Promise.&lt;boolean&gt;</code>
        * [.setGuilds([options])](#Client+setGuilds) ⇒ <code>Promise.&lt;object&gt;</code>
        * ["ready"](#Client+event_ready)
        * ["cacheUpdate"](#Client+event_cacheUpdate)
        * ["post"](#Client+event_post)
    * _static_
        * [.endpoint](#Client.endpoint) : <code>string</code>
        * [.isObject(obj)](#Client.isObject) ⇒ <code>boolean</code>

<a name="new_Client_new"></a>

### new Client([options])

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>ClientOptions</code> | <code>ClientOptions.default</code> | The configuration options. |

<a name="Client+options"></a>

### client.options : <code>ClientOptions</code>
The Client Options.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+bots"></a>

### client.bots : <code>Store.&lt;string, Bot&gt;</code>
Cached bots that are listed on the site, mapped through bot IDs.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+emojis"></a>

### client.emojis : <code>Store.&lt;string, Emoji&gt;</code>
Cached emojis that are listed on the site, mapped through emoji IDs.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+guilds"></a>

### client.guilds : <code>Store.&lt;string, Guild&gt;</code>
Cached guilds that are listed on the site, mapped through guild IDs.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+readyAt"></a>

### client.readyAt : <code>Date</code>
Date when Client was initially ready.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+readyTimestamp"></a>

### client.readyTimestamp : <code>number</code>
The timestamp when Client was initially ready.

**Kind**: instance property of [<code>Client</code>](#Client)
<a name="Client+edit"></a>

### client.edit([options], [preset]) ⇒ <code>ClientOptions</code>
Edit at least one or more key-value pair in the instance.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>ClientOptions</code> - The new client options.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>ClientOptions</code> | <code>ClientOptions.default</code> | A thing. |
| [preset] | <code>boolean</code> | <code>false</code> | Whether or not to have preset rules when setting values. |

**Example**
```js
console.log(Client.edit({ log: false }).options);
```
<a name="Client+fetchAllBots"></a>

### client.fetchAllBots(options) ⇒ <code>Promise.&lt;Array.&lt;Bot&gt;&gt;</code>
Returns all bots on the site.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Array.&lt;Bot&gt;&gt;</code> - All bots on the site.

| Param | Type | Description |
| --- | --- | --- |
| options | <code>FetchOptions</code> | Fetch Options. |

<a name="Client+fetchAllGuilds"></a>

### client.fetchAllGuilds(options) ⇒ <code>Promise.&lt;Array.&lt;Guild&gt;&gt;</code>
Fetches all guilds on the site.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Array.&lt;Guild&gt;&gt;</code> - All guilds on the site.

| Param | Type | Description |
| --- | --- | --- |
| options | <code>FetchOptions</code> | Fetch Options |

<a name="Client+fetchAllEmojis"></a>

### client.fetchAllEmojis(options) ⇒ <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code>
Fetch all emojis listed on the site.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code> - All emojis on the site.

| Param | Type | Description |
| --- | --- | --- |
| options | <code>FetchOptions</code> | Fetch Options. |

<a name="Client+fetchBot"></a>

### client.fetchBot(botID, [options]) ⇒ <code>Promise.&lt;Bot&gt;</code>
Fetch a bot from the site.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Bot&gt;</code> - Returns the bot contents/specified item.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| botID | <code>string</code> |  | The bot ID to fetch from the list. |
| [options] | <code>FetchOptions</code> | <code>{}</code> | FetchOptions. |

**Example**
```js
Client.fetchBot('463803888072523797', { specified: 'username' })
 .then(username => console.log(username))
 .catch(console.log);
```
<a name="Client+fetchEmoji"></a>

### client.fetchEmoji(emojiID, options) ⇒ <code>Promise.&lt;Emoji&gt;</code>
Fetch an emoji listed on the site.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Emoji&gt;</code> - Returns the emoji contents/specified item.

| Param | Type | Description |
| --- | --- | --- |
| emojiID | <code>string</code> | The emoji ID to fetch. |
| options | <code>FetchOptions</code> | Fetch Options. |

<a name="Client+fetchGuild"></a>

### client.fetchGuild(guildID, [options]) ⇒ <code>Promise.&lt;Guild&gt;</code>
Fetch a guild on the list.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Guild&gt;</code> - Returns the guild contents/specified item.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| guildID | <code>string</code> |  | The guild ID to fetch from the list. |
| [options] | <code>FetchOptions</code> | <code>{}</code> | Supply if you want to get a specific value, etc. 'prefix' |

<a name="Client+fetchGuildEmojis"></a>

### client.fetchGuildEmojis(guildID, options) ⇒ <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code>
Fetches a guild's emojis.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Array.&lt;Emoji&gt;&gt;</code> - The array of the guild's emojis.

| Param | Type | Description |
| --- | --- | --- |
| guildID | <code>string</code> | The guild ID to fetch its emojis from. |
| options | <code>FetchOptions</code> | Fetch Options. |

<a name="Client+fetchSelf"></a>

### client.fetchSelf([options]) ⇒ <code>Promise.&lt;Bot&gt;</code>
Fetch a bot using the ID supplied on initialization.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Bot&gt;</code> - Returns the bot contents/specified item.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>FetchOptions</code> | <code>{}</code> | Options. |

<a name="Client+fetchStats"></a>

### client.fetchStats([options]) ⇒ <code>Promise.&lt;Stats&gt;</code>
Fetch the site statistics.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Stats&gt;</code> - Returns site stats/specified value.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>FetchOptions</code> | <code>{}</code> | Supply if you want a specific value, etc. 'guilds' or 'bots' |

<a name="Client+fetchUpvotes"></a>

### client.fetchUpvotes([options]) ⇒ <code>Promise.&lt;Array.&lt;PartialUser&gt;&gt;</code>
Fetch users in the last 24 hours who have upvoted your bot.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;Array.&lt;PartialUser&gt;&gt;</code> - The array of the user objects/user IDs.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>UpvoteFetchOptions</code> | <code>{}</code> | Upvote Fetch Options. |

**Example**
```js
Client.fetchUpvotes({ ids: true });
```
<a name="Client+fetchUser"></a>

### client.fetchUser(userID, [options]) ⇒ <code>Promise.&lt;User&gt;</code>
Fetches a user that had logged on to botlist.space

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;User&gt;</code> - Returns the user contents/specified item.

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| userID | <code>string</code> |  | The user ID to fetch. |
| [options] | <code>FetchOptions</code> | <code>{}</code> | FetchOptions. |

<a name="Client+hasUpvoted"></a>

### client.hasUpvoted(userID) ⇒ <code>Promise.&lt;boolean&gt;</code>
Checks if a user has upvoted your bot.

**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;boolean&gt;</code> - Whether or not the user has upvoted your bot.

| Param | Type | Description |
| --- | --- | --- |
| userID | <code>string</code> | The user ID to check if they have upvoted your bot. |

<a name="Client+setGuilds"></a>

### client.setGuilds([options]) ⇒ <code>Promise.&lt;object&gt;</code>
**Kind**: instance method of [<code>Client</code>](#Client)
**Returns**: <code>Promise.&lt;object&gt;</code> - Returns the code, and a message.
**Emits**: [<code>post</code>](#Client+event_post)

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [options] | <code>PostOptions</code> |  | Post Options. |
| [options.token] | <code>string</code> | <code>&quot;this.options.token&quot;</code> | The API token for posting. |
| [options.botID] | <code>string</code> | <code>&quot;this.options.botID&quot;</code> | The bot ID for posting. |
| [options.guildSize] | <code>string</code> |  | The number (if no shards)/an array of numbers (if shards) to push to the API. Unneeded if a client was supplied. |

<a name="Client+event_ready"></a>

### "ready"
Emitted when cache is ready/cache was never run but it still returned something.

**Kind**: event emitted by [<code>Client</code>](#Client)
**Properties**

| Name | Type |
| --- | --- |
| bots | <code>Store.&lt;string, Bot&gt;</code> |
| guilds | <code>Store.&lt;string, Guild&gt;</code> |
| emojis | <code>Store.&lt;string, Emoji&gt;</code> |

<a name="Client+event_cacheUpdate"></a>

### "cacheUpdate"
Emitted when cache is updated.

**Kind**: event emitted by [<code>Client</code>](#Client)
**Properties**

| Name | Type |
| --- | --- |
| bots | <code>Store.&lt;string, Bot&gt;</code> |
| guilds | <code>Store.&lt;string, Guild&gt;</code> |
| emojis | <code>Store.&lt;string, Emoji&gt;</code> |

<a name="Client+event_post"></a>

### "post"
Emitted when a post is performed.

**Kind**: event emitted by [<code>Client</code>](#Client)
**Properties**

| Name | Type |
| --- | --- |
| code | <code>number</code> |
| message | <code>string</code> |

<a name="Client.endpoint"></a>

### Client.endpoint : <code>string</code>
The endpoint URL, used to interact with the site.

**Kind**: static property of [<code>Client</code>](#Client)
<a name="Client.isObject"></a>

### Client.isObject(obj) ⇒ <code>boolean</code>
Checks whether or not a given item is an object.

**Kind**: static method of [<code>Client</code>](#Client)
**Returns**: <code>boolean</code> - Whether or not the item that is testifyed is an object.

| Param | Type | Description |
| --- | --- | --- |
| obj | <code>object</code> | The item to testify against. |