# movieclip #

An updated version of the Movieclip library for Corona SDK

## How to use ##

Copy the `movieclip.lua` file to your project folder.

### Load the library ###

    local movieclip = require("movieclip.lua")
	
### Create the animation ###

    local images = { "frame1.jpg", "frame2.jpg", "frame3.jpg" }
    local animation = movieclip.newAnimation(images, 100, 100)
	
### Play the animation ###

	animation:play({
		remove = true, time = 4000, loop = 1
	})
	
### Create a weighted animation ###

    local frames = { 
		{ name = "frame1.jpg", weight = 1.5 }
		{ name = "frame2.jpg", weight = 0.3 }
		"frame3.jpg" # uses default weight of 1
	}
    local animation = movieclip.newAnimation(frames, 100, 100)

### Stop the animation ###

    animation:stop()
	
### Add the animation to a group ###

The `newAnimation` function will return a Display Object which can be added to a group.

    local images = { "frame1.jpg", "frame2.jpg", "frame3.jpg" }
    local animation = movieclip.newAnimation(images, 100, 100)
	g:insert(animation)

