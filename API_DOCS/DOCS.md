# Client
###### The class for interacting with botlist.space

* Static References
    * [Client.Classes]()
    * [Client.endpoint]()
* Instance References
    * [Client.edit](#Edit)
    * [Client.fetchAllBots()]
    * [Client.fetchAllEmojis()]
    * [Client.fetchAllGuilds()]
    * [Client.fetchBot()]
    * [Client.fetchEmoji()]
    * [Client.fetchGuild()]
    * [Client.fetchGuildEmojis()]
    * [Client.fetchSelf()]
    * [Client.fetchStats()]
    * [Client.fetchUpvotes()]
    * [Client.fetchUser()]
    * [Client.hasUpvoted()]
    * [Client.setGuilds()]

## Instance Functions

### Client.edit(options, ?preset) => ClientOptions

Edits the Client Options that were supplied on initialization.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|options| |Object|The options to replace the existing options.|
|preset|false|Boolean|Whether or not to replace all options with their default parameters, then override them with ``options``|

### Client.fetchAllBots(?options) => Promise<Array<Bot>>

Fetches all bots that are listed on the site.

|Parameter|Default|Type|Description
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|
|options.normal|false|Boolean|Whether or not to return the plain objects.|
|options.specified|false|String|The specified value that is desired to be fetched.|
|options.stringify|false|Boolean|Whether or not to return the bot's mention string.|

### Client.fetchAllEmojis(?options) => Promise<Array<Emoji>>

Fetches all emojis that are listed on the site.

|Parameter|Default|Type|Description
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|
|options.normal|false|Boolean|Whether or not to return the plain objects.|
|options.specified|false|String|The specified value that is desired to be fetched.|
|options.stringify|false|Boolean|Whether or not to return the text that turns into an emoji when used in a Discord Message.|

### Client.fetchAllGuilds(?options) => Promise<Array<Guild>>

Fetches all Guilds (servers) that are listed on the site.

|Parameter|Default|Type|Description
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|
|options.normal|false|Boolean|Whether or not to return the plain objects.|
|options.specified|false|String|The specified value that is desired to be fetched.|
|options.stringify|false|Boolean|Whether or not to return the Guild Name.|

### Client.fetchBot(botID, ?options) => Promise<Bot>

Fetches a Bot that is listed on the site.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|botID| |String|The Bot ID to be used to fetch the desired Bot.
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchEmoji(emojiID, ?options) => Promise<Emoji>

Fetches an Emoji that is listed on the site.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|emojiID| |String|The Emoji ID to be used to fetch the desired Emoji.
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchGuild(guildID, ?options) => Promise<Guild>

Fetches a Guild that is listed on the site.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|guildID| |String|The Guild ID to be used to fetch the desired Guild.
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchGuildEmojis(guildID, ?options) => Promise<Array<Emoji>>

Fetches a guild's emojis that are listed on the site.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|guildID| |String|The Guild ID to be used to fetch the desired Guild's Emojis.
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchSelf(?options) => Promise<Bot>

Fetches a Bot using ``this.options.botID``

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchStats(?options) => Promise<Stats>

Fetches the Site's Statistics.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchUpvotes(?options) => Promise<Array<PartialUser>>

Fetches a Bot's upvotes. **Requires an API Token**

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|options|{}|FetchOptions|Fetch Options.|

### Client.fetchUser(userID, ?options) => Promise<User>

Fetches a User that has logged onto the site.

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|userID| |String|The User ID to be used to fetch the desired User.
|options|{}|FetchOptions|Fetch Options.|

### Client.hasUpvoted(userID) => Promise<Boolean>

Checks whether or not a user has upvoted your bot. **Requires an API Token**

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|userID| |String|The User ID to be used to check whether or not the user has upvoted.

### Client.setGuilds(?options) => Promise<Object>

Posts your Bot's Server Count onto the site. **Requires an API Token**

|Parameter|Default|Type|Description|
|:--:|:--:|:--:|:--:|
|options|{}|PostOptions|Post Options.