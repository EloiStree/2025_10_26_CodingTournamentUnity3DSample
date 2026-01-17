You want to create a coding tournament game ?

What you will need is input that dont hack your game.

## Some input to play the game

I am using the IID format.

Index,int: player given network index
Value,int: integer that representa action in your game
Date, ulond: timestramp representing when to do the action with NTP UTC

# Some Timing to synchronise player and server

You are going to need NTP adjustment to make sure your time is the same as the other player.
Having the same NTP time allows some crazy magic shit when you think a bit about it.


# Some player positions and game info

## As bytes

When you have 256 players... You are going to need bytes and not text.

So push Type of Data (int) | Format Used (int) | Number Of Player (int) | All players as bytes

Be careful to not push 60 fps the data, you have to transport all that in the Wifi.

Outside of a LAN logic you can update position of object in your game... To much data.
So for bullets, I tip your to provide size, start origine, speed and timestramp ntp

## As Text

All games you are going to build are going to have even, gameinfo, log and stuffs.

IT is going to be a mess. so given manual with that.

You can store the player position as text if you are under 16 player. But I would not do that for more.


# To complete




The idea of this file is to list outside of UPD Websocket the tranfict to support.
To make an abstract layer for the code tournament we want to organise and lets the community mod around.