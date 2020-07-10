
# Welcome to Day 10 of the Clemson Game Coding Camp!
-Richard Knoll talk 

  - Day 10 (Conner)
    - Standup Scrum for everyone
    - Multi-player games
    - Networking
      - Moving data between computers.
        - I would assume that most kids would have a vague understanding of the internet, is there something we can say here that would be informative but also not be too in-depth for the shortened time period?
      - Goals
        - Why might we introduce networking to a game?
        - Interact with players on their own computers. Ask the players to name a couple popular multiplayer games
          - Halo, Chess, Minecraft
          - Fortnite will probably be named, that&#39;s a good one since it has so much data to transfer
        - Interacting in a game world that&#39;s too big for your computer.
          - Minecraft, World of Warcraft, Star Citizen, No Man&#39;s Sky

      - Multiplayer games
        - Showing my character&#39;s animation/motion to another player on a different computer.
          - How could this work (speculation is ok)?
          - Use Minecraft to demonstrate
            - [https://minecraft.gamepedia.com/Classic\_server\_protocol](https://minecraft.gamepedia.com/Classic_server_protocol)
            - Load into some popular Minecraft server
              - Each one has some sort of way to ensure that they are managing load effectively
            - Demonstrate how the chunks (areas of land) are used to limit client and server load, talk about why
              - Server only sends player enough information for one chunk
              - Server only sends updates for players in their view distance (chunk range)
            - Talk about how chunks are transferred (this is speculation)
              - Large amounts of data will be transferred in blocks to the client for terrain information
              - After the initial terrain information has been loaded, the server sends differential updates to the client about how the terrain has changed. (a player has placed or removed a block, TNT, etc...)
            - Small chunks of data are transferred to indicate player coordinates and current action state (walk, run, hitting, mining)
        - Constraints
          - Low latency
          - Eventual consistency - Handling Race Conditions?
          - How much data and algorithms are shared between the computers and how much needs to be transmitted.

      - Hosted games
        - No Man&#39;s Sky is a great example of this, it is multiplayer, but it is impossible to install on one machine due to size constraints
        - How might this work? Again Speculation
          - The world isn&#39;t real, or stored anywhere, instead an algorithm is used to procedurally generate the environment only when the player is viewing them.
          - If the environment isn&#39;t stored anywhere then how does the game handle changes that have been made to the environment?
            - The game stores differentials from the output that the algorithm generates, then replays these changes to give the effect that it was stored the entire time.
        - Constraints
          - The amount of data transferred from the server to the client has to be minimal enough so that the additional time spent loading a hosted resource is not outweighed by the cost of downloading the resource to the client&#39;s machine.

    - Work with Partner on Game
      - Hour 1 Scrum
      - Hour 2 Scrum
      - Hour 3 Scrum
   
