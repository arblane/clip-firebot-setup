# clip-firebot-setup

# Description
Firebot setup for playing Twitch clips on stream from user input.

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
+ Toggle enabled/disabled is controlled by an effect list
  + Add it to a startup event to disable on launch of Firebot (not included in the setup)
  + An event on startup of OBS is included to reset the clips played this stream session
+ An overlay instance is provided to keep the effect separate from any other effect overlays, useful when you want to stop playing clips early.
+ Effect has a date range filter of the past 12 months
+ The html/css file will make use of the targeted streamer's color to generate a gradient background
+ Customize:
  + the size and position to your liking
  + the html file location
  + the date filter: shorter, longer, or disable
  + there is a 'broken image' image in the game box art img tag that needs to be customized

# Credits
+ Inspired by: MattyCanny
+ Coding elements: Raimen
