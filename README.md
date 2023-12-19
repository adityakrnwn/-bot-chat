const { Client, Intents, Message } = require('discord.js');
const client = new Client({
  intents: [
    Intents.FLAGS.GUILDS,
    Intents.FLAGS.GUILD_MESSAGES
  ]
});

const token = 'MTE4NjI5MDk5NzE4MTgxNjkzMw.GBaDsf.Fr6ZL_zhqoKFgiIZC5YuMJ8q8DGrUENbnleb2Y';

client.on('ready', () => {
    console.log('Bot ${client.user.tag} telah login!');
});

client.on('messageCreate', (message) => {
    if (message.content === 'hallo') {
        message.reply('hallo juga kak');
    }
    if (message.content === '!ping') {
        message.reply('Pong!');
    }
})

client.login(token);
