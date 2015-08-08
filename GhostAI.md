# Introduction #

This section outlines the AI that the ghosts will follow in order to decide how to best move.

# Details #

In order to decide where each ghost should move to, all possible directions are assessed for possibility of movement.  First, the ghost will attempt to move in a direction, and if the direction is valid (no wall), then the spot where the ghost would move to is used to calculate a distance associated with that direction of movement.  The distance is found via trigonometry magic.  Then, depending on pacman's state, ghosts will take a path.

**The Trigonometry Magic:**

We form a triangle between pacman and the ghost, and then we find the hypotenuse.

absolute value of pacman.x - ghost.x = DeltaX
absolute value of pacman.y - ghost.y = DeltaY

Distance = root (DeltaX<sup>2</sup> + DeltaY<sup>2</sup>)

Where the ghosts go depends on whether pacman is in BEAST MODE or not.  If pacman is hopped up on drugs and raging around, then the ghosts run away, taking the path that puts them furthest from pacman each square.

If pacman has sobered up, and isn't raging around, then the ghosts take the square that puts them closest to pacman each movement they take.

Ghosts are DISCOURAGED from turning around directly.  They CAN if they are some how cornered and turning directly around is the only path.