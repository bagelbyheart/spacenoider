# spacenoider

A pico-8 game by [@bagelbyheart](https://twitter.com/bagelbyheart) based roughly on arcade games like Galaga and Asteroids.

## Current Status

Right now I'm in the process of refactoring Spacenoider so it can be expanded into a more elaborate arcade shmup. The original version was really just a chance for me to play with "particle" systems. Since then I've been working to move all objects into a single table and reuse more code.

## Major items

The following are big things that need to be addressed in a rough order of ease.

1. Make drops more direct clones of generic entities.  
  * _gendrop is basically a dupe of genent right now._
2. Unify all objects with drops. ie, there should be a drop version of everything that appears on screen that causes you to shoot that same object, which in turn means I need to encode the drop icon in the object.

The stuff past this is what I want to do after finishing the refactor.

1. Add power-ups for each weapon.
2. Have weapons and power-ups change player appearance.
3. Model enemies off how they modify the player.  
  * _I'm not sure what I meant by this..._

## Fixing drops

### Within `gendrop`

1. `drop.sx` and `sy` should be replaced with `xd yd`
2. `w and h` don't need to be defined in the generic drop
3. same with `spd`.
4. `act` can be replaced with `onhit`
5. Does `gendrop` really need it's own update function?
  * Can probably move the expiration into the `mov` function
  * this would be even more clever if I switch to a moves table
6. The dedicated draw function is probably easiest for now.

### Within specific drops

1. x,y can be have the "or" sections removed, we aren't going to make them without
2. the `drnd()` for `sx and sy` should be moved into the movement type
3. instead of per drop functions there should just be a `dmake(en,x,y,more)` function.
