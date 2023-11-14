# Portfolio
This is a collection of all the notable projects that I have done with explanations and links to the GitHub repos of the corresponding projects.

# Unity FPS Game
Includes usage of the unity animation, pathfinding, and audio systems.

Game was fully completed with menu’s, UI, and a full playable level

AI design:
- AI would transition between different states based on HP (e.g. aggressive, running away, etc.)
- Within a particular state the AI would go through a decision tree to determine next move. This would take into account the enemy’s current health, distance to player, and distance to different “shooting points” and “cover points” which would be placed around the map
- For example, if the enemy’s health gets too low it will begin retreating to cover as demonstrated in following slides. See video on GitHub
