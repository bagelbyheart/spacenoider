# spacenoider

A pico-8 game by [@bagelbyheart](https://twitter.com/bagelbyheart) based roughly on arcade games like Galaga and Asteroids.

## Current Status

Right now I'm in the process of refactoring Spacenoider so it can be expanded into a more elaborate arcade shmup. The original version was really just a chance for me to play with "particle" systems. Since then I've been working to move all objects into a single table and reuse more code.

## Major items

The following are big things that need to be addressed in a rough order of ease.

1. Replace `function(self) return null end` blocks with a dedicated function and reference that.
1. Make global bounding based on ACTUAL space left.
2. Make a merge table function to replace all of my `for k,v in pairs(tbl) do e[k]=v end` chunks.
3. Unify all objects with drops. ie, there should be a drop version of everything that appears on screen that causes you to shoot that same object, which in turn means I need to encode the drop icon in the object.

The stuff past this is what I want to do after finishing the refactor.

1. Add power-ups for each weapon.
2. Have weapons and power-ups change player appearance.
3. Model enemies off how they modify the player.
