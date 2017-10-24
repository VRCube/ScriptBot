[download]: https://img.shields.io/badge/download-Spigot-orange.svg
[license]: https://img.shields.io/badge/License-Apache%202.0-lightgrey.svg
[discord-invite]: https://discord.gg/AdmWkEs
[ ![download][] ](https://github.com/VRCube/ScriptBot/)
[ ![license][] ](https://github.com/VRCube/ScriptBot/tree/master/LICENSE)
[ ![Discord](https://discordapp.com/api/guilds/316647825553358848/widget.png) ][discord-invite]

# ScriptBot
A Discord bridge bot for spigot and discord, 100% Customizable, Custom script for JDA Events and Bukkit
## Configuration
```yaml
# ScriptBot by VRCube
# For info on bot, please go to https://github.com/DV8FromTheWorld/JDA/
# For example on script, please go to https://github.com/VRCube/ScriptBot
# Bot info
bot-token: 'Insert token here'
bot-playing: 'Minecraft'
# This is import for command script
# DO NOT REMOVE JAVA.LANG.* OR ELSE NOTHING WILL WORK!
script-imports:
  - java.lang.*
  - java.utils.*
  - org.bukkit.*
  - org.bukkit.block.*
  - org.bukkit.entity.*
  - org.bukkit.inventory.*
  - org.bukkit.material.*
  - org.bukkit.map.*
  - org.bukkit.util.*
  - org.bukkit.scheduler.*
  - org.bukkit.plugin.*
  - org.bukkit.scoreboard.*
  - net.dv8tion.jda.core.*
  - net.dv8tion.jda.core.hooks.*
  - net.dv8tion.jda.core.utils.*
  - net.dv8tion.jda.core.events.message.*
  - net.dv8tion.jda.core.events.guild.*
  - net.dv8tion.jda.core.events.channel.*
  - net.dv8tion.jda.core.events.*
  - net.dv8tion.jda.core.entities.*
  - net.dv8tion.jda.bot.*
  - net.dv8tion.jda.client.*
  - org.bukkit.event.*
  - org.bukkit.entity.*
  - org.bukkit.event.player.*
  - org.bukkit.event.block.*
  - org.bukkit.event.entity.*
  - org.bukkit.event.enchantment.*
  - org.bukkit.event.hanging.*
  - org.bukkit.event.inventory.*
  - org.bukkit.event.server.*
  - org.bukkit.event.vehicle.*
  - org.bukkit.event.world.*
  - me.vrcube.scriptbot.*


# Use message with only type MSG
# Use script with only type SCRIPT
# Put script files in plugins/ScriptBot/scripts
# Put delete: true to delete command after sent

# Example for scripts
#commands:
#  '!players':
#    type: SCRIPT
#    script: 'players.java'
#    delete: true
# in players.java you can write code there, no need methods
# bindings that are available:
# event   - MessageReceivedEvent
# channel - MessageChannel
# bot     - JDA: the bot itself
# author  - User: Command sender
# message - Message

commands:
  '!ping':
    type: MSG
    message: 'hello'

# Bukkit Events
# To get bot instance, use ScriptBot.getBot()
# To listen for event, use the way you did with Bukkit
# Example:
# @EventHandler
# public void onJoin(PLayerJoinEvent event){
#   System.println("A player joined: "+event.getPlayer().getName());
#}
# put script in plugins/ScriptBot/scripts
event-script: 'none'

# JDA Events
# To get bot instance, use event.getJDA()
# Use method overrides from ListenerAdapter class
# Events can be found here: https://github.com/DV8FromTheWorld/JDA/tree/master/src/main/java/net/dv8tion/jda/core/events
# Some event classes are not imported, if you wish to use it. Import it
# Example:
# @Override
# public void onMessageReceived(MessageReceivedEvent event){
#   Bukkit.broadcastMessage("Message received! "+event.getMessage().getRawContent());
# }

jda-event-script: 'none'
```
## Examples
Examples can be found [here](https://github.com/VRCube/ScriptBot/tree/master/examples)
