# Portfolio
Welcome to my portfolio! This is a collection of all the notable projects that I have done.

Please feel free to use the the table of contents to jump around to the areas you're interested in.

**Important**, this page is still under development and is being updated regularly. The following features are yet to be implemented:
- Not all sections contains links to GitHub repos. This is likely because they are using a different or no source control soltion and have not yet been ported to GitHub. Notably, projects developed in Unity used PlasticSCM for source control instead of GitHub
- Some projects are still missing such as my web development projects Treoguessr and Munch Meter. These will be added soon

<br>

# Contents

- [Unity FPS Game](#unity-fps-game)
- [Unity Co-op Shooter](#unity-co-op-shooter)
- [Custom Game Engine in C++ and OpenGL](#custom-game-engine-in-c-and-opengl)
- [Networked Messaging Application](#networked-messaging-application)

<br>

# Unity FPS Game

**Tags**: *Unity, C#, AI*

Includes usage of the unity animation, pathfinding, and audio systems.

Game was fully completed with menu’s, UI, and a full playable level

AI design:
- AI would transition between different states based on it's health points (e.g. aggressive, running away, etc.)
- Within a particular state the AI would go through a decision tree to determine next move. This would take into account the enemy’s current health, distance to player, and distance to different “shooting points” and “cover points” which would be placed around the map
- For example, if the enemy’s health gets too low it will begin retreating to cover as demonstrated in the following video.

https://github.com/YusufHussain242/Portfolio/assets/71587676/bbbb4b82-3f79-4181-93fa-01e12837857c

<br>

# Unity Co-op Shooter

**Tags**: *Unity, C#, Networking*

Note that unlike the previous, this game is not complete and is still under development. Therefore, there are no models or textures in the game

The game involved a team of 4 players, completing a series of challenges and puzzles with a heavy emphasis on teamwork and communication to succeed.

Networking was implemented using the Photon Pun API, which is similar to a peer-peer networking solution, however it uses a dedicated relay server to relay messages between clients.

For this reason, I am planning to migrate to using the Fishnet API and creating my own matchmaking server to connect users, using techniques such as hole punching.

The challenge in the first level is a Simon says type encounter where up to 7 “oracles” will appear in a given order around the map, and the players have to shoot these oracles in the order they appear. However, the oracles are placed around the map such that no-one will be able to see all the oracles at any given time, and so must communicate the locations of the oracles and coordinate when to shoot.

Creating a video demonstration for the level is difficult as it requires a full team of 4, therefore a gameplay video of the first level has not yet been created. I will add the video to this page as soon as I gather 4 people to create the demonstration. However, I can still demonstrate how the multiplayer functionality works locally which is shown in the following video.

https://github.com/YusufHussain242/Portfolio/assets/71587676/0b74ca4a-a9bf-4920-8b2e-31a72000f82f

<br>

# Custom Game Engine in C++ and OpenGL

**Tags**: *C++, OpenGL, Systems-Level, OOP*

[(Visit the Repo Here)](https://github.com/YusufHussain242/GameEngine)

While the game engine did involve using and understanding many of the complexities of OpenGL such as shaders, index buffers, and vertex array objects, you can see that the engine is not very graphically complex. This is because graphics rendering was not the main goal of the engine.

The main goal of the engine was to produce a suite of game development tools, to create a game development framework which produces a workflow similar to the one found in unity. These tools include a component system, entity management system, and a collision detection system.

Implemented ray casts for collision detection using vector mathematics. More detail will be added soon.

The following is a short video of a sample level made in my custom game engine.

https://github.com/YusufHussain242/Portfolio/assets/71587676/190cc0f8-051e-47e3-a336-117e96284e01

<br>

# TCP Based Webserver

**Tags**: *C#, Sockets, Networking, Systems-Level*

[(Visit the Repo Here)](https://github.com/YusufHussain242/OnlineMessenger)

Multi-threaded webserver can handle multiple clients simultaneously, managing multiple sessions where clients and communicate with other clients in the session.

The Webserver is capable of recieving multiple different kinds of data such as strings and ints, as well larger C# objects containing multiple fields and broadcasting them to clients within a session.

The C# objects are serialized data optimally to minimise payload size, making the server as efficient as possible. This is significantly faster than using JSON for example.

Original intention was to be used for real-time data transmission between players in one of the Unity games above. However, in the end I opted to use one of the public API’s instead as they were more feature rich.

I should make clear that this is not a HTTP webserver, those are more focused on versatility and are to be used for web development. My webserver is focused maximising performance for potential application in real time data transmission.

![MessagingAppExample](https://github.com/YusufHussain242/Portfolio/assets/71587676/855f2974-9a83-4f97-a36a-46edde2083ba)


