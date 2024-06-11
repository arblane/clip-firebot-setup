# clip-firebot-setup

# Description
Firebot setup for playing Twitch clips on stream from user input.

# Compatibility
- Firebot 5.62.1+

# Install
+ Download
  + Clip.firebotsetup
  + clips.html
+ Import the downloaded firebotsetup file
  + You will be prompted to change the location of the html file during import.

# Usage

## Requirements for Chat
+ Must be following the channel
+ Command/Effect will prevent clips 
  + from the same streamer twice in a row
  + duplicate clips per stream session
+ Cooldown to prevent chat from spamming, currently 10 seconds per user

## Commands for Chat
+ !clip 
  + streamer name with or without the leading @ symbol
  + url either:
    + https://www.twitch.tv/
    + https://clips.twitch.tv/

## Streamer Info
+ Toggle enabled/disabled is controlled by an effect list
  + Add it to a startup event to disable on launch of Firebot (not included in the setup)
  + Add it to an event on startup of OBS to reset the clips played this stream session
+ An overlay instance is provided to keep the effect separate from any other effect overlays, useful when you want to stop playing clips early.
+ Effect has a date range filter of the past 12 months
  + You can toggle this on/off in '[API] Get User Clips' preset effect
+ The html/css file will make use of the targeted streamer's color to generate a gradient background
+ Utilities included
  + [Utility] Clip Uri Details
    + Gets the clip ID to add to the tracking list of clips
  + [Utility] Clip Duration Filter
    + Customizable filter to limit the duration of the clips chosen
  + [Utility] Reset Clips Played this Stream
    + Resets the tracking list of clips played this stream to prevent duplicates
  + [TP] ToggleClip
    + Sets a toggle to enable/disable clips
  + [TP] Stop Current Clips
    + Clears any clips playing from the queue
+ Customize:
  + the size and position to your liking
  + the date filter: shorter, longer, or disable (in [API] Get User Clips)
  + the number of clips to pull, default 100 (in [API] Get User Clips)
  + the max duration of clips to pull, or disable (in [API] Clip Duration Filter)
  + there is a 'broken image' image in the game box art img tag that needs to be customized

# Additional
+ This is a complete setup, if you want to put your own version together, check out the following repo's for modular pieces used by this setup
  + [API-Random-Twitch-Clip](https://github.com/arblane/API-Random-Twitch-Clip)
  + [API-Twitch-Game-Info](https://github.com/arblane/API-Twitch-Game-Info)

# Credits
+ Inspired by: MattyCanny
+ Coding elements: Raimen
