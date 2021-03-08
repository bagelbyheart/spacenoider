# spacenoider

A pico-8 game by [@bagelbyheart](https://twitter.com/bagelbyheart) based roughly on arcade games like Galaga and Asteroids.

## Current Status

Right now I'm in the process of refactoring Spacenoider so it can be expanded into a more elaborate arcade shmup. The original version was really just a chance for me to play with "particle" systems. Since then I've been working to move all objects into a single table and reuse more code.

### Major Items

The following are big things that need to be addressed in a rough order of ease.

1. Revamp spawn functions to be more precise. Currently just `_sline` and `dline`.
2. Make movement accept tables of movement types.
3. Unify all the `nmake()` functions.  
  * This should be easy enough, pmake is the only one that doesn't already accept an `en` argument, and doing so allows things like player select later on.
  * I can store the template function in the entity table.

### Ugh Items

These are things that I would like to do, but seem overwhelming at the moment.

1. Unify all objects with drops. ie, there should be a drop version of everything that appears on screen that causes you to shoot that same object, which in turn means I need to encode the drop icon in the object.

### Stretching Items

The stuff past this is what I want to do after finishing the refactor.

1. Add power-ups for each weapon.
2. Have weapons and power-ups change player appearance.
3. Model enemies off how they modify the player.  
  * _I'm not sure what I meant by this..._

