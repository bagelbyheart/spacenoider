# spacenoider

A pico-8 game by [@bagelbyheart](https://twitter.com/bagelbyheart) based roughly on arcade games like Galaga and Asteroids.

## Current Status

Right now I'm in the process of refactoring Spacenoider so it can be expanded into a more elaborate arcade shmup. The original version was really just a chance for me to play with "particle" systems. Since then I've been working to move all objects into a single table and reuse more code.

### Ugh Items

These are things that I would like to do, but seem overwhelming at the moment.

1. Unify all objects with drops. ie, there should be a drop version of everything that appears on screen that causes you to shoot that same object, which in turn means I need to encode the drop icon in the object.

### Stretching Items

The stuff past this is what I want to do after finishing the refactor.

1. Add power-ups for each weapon.
2. Have weapons and power-ups change player appearance.  
  * This should be pretty easy since drops can do things like alter the player sprite table, although failing back that way might be harder...
3. Model enemies off how they modify the player.  
  * _I'm not sure what I meant by this..._
  * Maybe, make the missile enemy look similar to how the missile power up makes the player look? Seems possible.


