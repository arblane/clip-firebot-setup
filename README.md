# clip-firebot-setup

# Description
Firebot setup for playing Twitch clips on stream from user input.

# Version
4

# Install
+ To install, download:
  + Clip.firebotsetup
  + clips.html
+ Import setup for Firebot by going to Settings > Setups > Import Setup.
  + Choose the file "Clip.firebotsetup" from the location you just downloaded it to, then click Import setup. 
  + You will need to edit the preset effect to change the location of the html file.

# Usage

## Requirements for Chat
+ Must be following the channel
+ Command/Effect will prevent clips 
  + from the same streamer twice in a row
  + duplicate clips per stream session
+ Cooldown to prevent chat from spamming, currently 20 seconds per user


## Commands for Chat
+ !clip (streamer name)

## Streamer Info
+ Toggle enabled/disabled is controlled by an effect list, add it to a startup event to disable on launch of Firebot
+ An overlay instance is provided to keep the effect separate from any other effect overlays, useful when you want to stop playing clips early.
+ Effect has a date range filter of the past 12 months
+ Customize:
  + the colors and position to your liking
  + the html file location
  + the date filter: shorter, longer, or disable

# Credits
+ Inspired by: MattyCanny
+ Coding elements: Raimen
