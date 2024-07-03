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
  + url either type:
    + https://www.twitch.tv/ or https://clips.twitch.tv/
    + url will be sanitized by the utility to remove extraneous information

## Streamer Info
+ An overlay instance is provided to keep the effect separate from any other effect overlays, useful when you want to stop playing clips early.
+ The html/css file will make use of the targeted streamer's color to generate a gradient background

+ Utilities included:
  + [Utility] Randomize Clips
    + Randomizes the clips
  + [Utility] Clip Duration Filter
    + Customizable filter to limit the duration of the clips chosen
    + Can be enabled/disabled
    + Default is 30 seconds
  + [Utility] Reset Clips Played this Stream
    + Resets the tracking list of clips played this stream to prevent duplicates
    + Info: You can add to an event on startup of OBS to reset the clips played this stream session.
  + [Utility] Clip Uri Details
    + Gets the clip ID to add to the tracking list of clips
  + [Utility] Clip Player
    + Uses the elements from the other utilities and the html to play the clip
  + [Variable] Clips Date filter
    + The date filter: shorter, longer, or disable (in [API] Get User Clips)
    + Can be enabled/disabled
    + Default is 
      + Enabled
      + Previous 12 months
  + [Variable] Clips No Date filter
    + Hets clips without date filter
    + Default is
      + Disabled
  + [TP] Toggle Clip
    + Sets a toggle to enable/disable clips
    + Info: You can add it to a startup event to disable on launch of Firebot.
  + [TP] Stop Current Clips
    + Clears any clips playing from the queue

+ Customize:
  + html
    + the size and position to your liking
    + the details you would like to include
    + there is a 'broken image' image in the game box art img tag that needs to be customized

# Additional
+ This is a complete setup, if you want to put your own version together, check out the following repo's for modular pieces used by this setup
  + [API-Random-Twitch-Clip](https://github.com/arblane/API-Random-Twitch-Clip)
  + [API-Twitch-Game-Info](https://github.com/arblane/API-Twitch-Game-Info)

# Credits
+ Inspired by: MattyCanny
+ Coding elements: Raimen
