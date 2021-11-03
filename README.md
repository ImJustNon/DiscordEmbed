## 1
```js
// at the top of your file
const { MessageEmbed } = require('discord.js');

// inside a command, event listener, etc.
const exampleEmbed = new MessageEmbed()
    .setColor('#0099ff')
    .setTitle('Some title')
    .setURL('https://discord.js.org/')
    .setAuthor('Some name', 'https://i.imgur.com/AfFp7pu.png', 'https://discord.js.org')
    .setDescription('Some description here')
    .setThumbnail('https://i.imgur.com/AfFp7pu.png')
    .addFields(
        { name: 'Regular field title', value: 'Some value here' },
        { name: '\u200B', value: '\u200B' },
        { name: 'Inline field title', value: 'Some value here', inline: true },
        { name: 'Inline field title', value: 'Some value here', inline: true },
    )
    .addField('Inline field title', 'Some value here', true)
    .setImage('https://i.imgur.com/AfFp7pu.png')
    .setTimestamp()
    .setFooter('Some footer text here', 'https://i.imgur.com/AfFp7pu.png');

channel.send({ embeds: [exampleEmbed] });

```


## 2
```js
const exampleEmbed = {
    color: 0x0099ff,
    title: 'Some title',
    url: 'https://discord.js.org',
    author: {
        name: 'Some name',
        icon_url: 'https://i.imgur.com/AfFp7pu.png',
        url: 'https://discord.js.org',
    },
    description: 'Some description here',
    thumbnail: {
        url: 'https://i.imgur.com/AfFp7pu.png',
    },
    fields: [
        {
            name: 'Regular field title',
            value: 'Some value here',
        },
        {
            name: '\u200b',
            value: '\u200b',
            inline: false,
        },
        {
            name: 'Inline field title',
            value: 'Some value here',
            inline: true,
        },
        {
            name: 'Inline field title',
            value: 'Some value here',
            inline: true,
        },
        {
            name: 'Inline field title',
            value: 'Some value here',
            inline: true,
        },
    ],
    image: {
        url: 'https://i.imgur.com/AfFp7pu.png',
    },
    timestamp: new Date(),
    footer: {
        text: 'Some footer text here',
        icon_url: 'https://i.imgur.com/AfFp7pu.png',
    },
};

channel.send({ embeds: [exampleEmbed] });
```
