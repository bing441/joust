# joust
A tutorial project that is sort-of-a-clone of the old arcade game Joust

[Joust on YouTube](https://www.youtube.com/watch?v=BWoiLNri0OM)

In terms of development, my plan is to tackle these things, in
the following order.

* Basic flying of the main player.  Taps on the left or right side of the screen will provide vertical acceleration, turn the player to face one way or another, and a bit of horizontal acceleration.  For starters, the bottom of the screen will absorb all acceleration, while the top will bounce.  Some friction each frame will cap the max speed, and I'll have a time-out on each "flap" so that just rapid tapping won't be a strategy.
* After that, add in some automated opponents.  They'll flap occasionally at random, flap more to come up to the same level as the player, and occasionally change directions (random).
* The players and opponents will all be derived from a (home brew) Sprite class.  I could use SpriteKit, but I'm hoping to demonstrate the mechanics under the hood (SpriteKit does all of this really nicely -- for a "pro" level game, that would be the right way to go).

I'll also include a singleton game state class.  It'll have an array of all the sprites on screen -- including the player.  Each frame, we'll apply acceleration as appropriate, move the sprites, check for collisions (and resolve), and then render everything.  

