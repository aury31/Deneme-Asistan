const Discord = require(`discord.js`)

exports.run = async(client, message)=> {
  
  let user = message.mentions.users.first() || message.author
  if(user){
    
const embed = new Discord.MessageEmbed()
 .setDescription(`${message.author.tag} adlı kullanıcının avatarı:`)
.setImage(user.displayAvatarURL({dynamic:true})) 
.setTimestamp()
.setColor(`YELLOW`)
.setFooter(`DarknessTR`)
message.channel.send(embed)
 } else {
  const embed = new Discord.MessageEmbed()
  .setDescription(`${message.author.tag} adlı kullanıcının avatarı:`)
.setImage(message.author.avatarURL({dynamic:true}))
.setTimestamp()
  .setColor(`YELLOW`)
.setFooter(`DarknessTR`)
message.channel.send(embed)
 }
};

exports.conf = {
    enabled: true,
    guildOnly: false,
    aliases: ["avatar","avatarım"],
    permLevel: 0
}

exports.help = {
    name: 'pp',

}client.on("message", async eren => {
let tag = "TAGINIZ"//TAGINIZI YAZINIZ//
if(eren.content == "${p}tag" || eren.content == "${p}tag" || eren.content == "${p}tag" || eren.content == "${p}Tag" || eren.content == "${p}TAG" || eren.content == "${p}TAG") {
let embed = new Discord.MessageEmbed()
.setTitle(tag)
.setDescription(`
**İşte tagimiz:**
\`${tag}\`
`)
eren.channel.send(embed)
} else return;
});const Discord = require("discord.js");
const db = require("quick.db");

exports.run = async (app, message, client) => {
  const erensy319= new Discord.MessageEmbed()
    .setColor("RANDOM")
    .setDescription("⚙️ **Ping Hesaplanıyor...**");

  let erensss = Date.now();
  let erenscode= await message.channel.send(erensy);
  let erensycoddee = Date.now() - erenss;
  let erensyAPI = app.ws.ping.toFixed(2);
  setInterval(() => {
    const erensembed = new Discord.MessageEmbed()
      .setDescription(
        `\n 💬  Mesaj Gecikme Süresi ; **${erensycoddee}Ms** \n\n 👁‍🗨 Bot Gecikme Süresi ; **${erensyAPI}Ms**`
      )
      .setColor("RANDOM");
    erensycode.edit(erensembed);
  }, 5000);
};
exports.conf = {
  enabled: true,
  guildOnly: false,
  aliases: ["ping"],
  permLevel: 0
};

exports.help = {
  name: "ping",
  description: "Ping komutu işte yaw",
  usage: "ping"
};
const Discord = require('discord.js')

exports.run = function(bot, message) {
    message.channel.send(new Discord.MessageEmbed()
    .setColor("RANDOM")
    .setTitle('🎲 Zarın: ' + doMagicDiceVoodoo()));

    function doMagicDiceVoodoo() {
        var random = ['1', '2', '3', '4', '5', '6','7','8','9','10','11','12'];

        return random[Math.floor(Math.random()*rand.length)];
    }
}

exports.conf = {
  enabled: true,
  aliases: ['zar','zatat'],
  guildOnly: false,
  permLevel: 0,
};

exports.help = {
  name: 'zar-at',
  description: 'Zar Atın',
  usage: ''
};
