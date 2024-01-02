Host Migration is a process in multiplayer games where the responsibility of the server is transferred from one host to another. This is typically done when the original host leaves the game or encounters an issue that prevents them from continuing to host the game.


!!!warning

Seamless Host Migration is not directly possible with Unreal Engine 5. This is because the game classes are destroyed when the host leaves the game. This means that the game state is lost and the new host will have to start a new game. This is a limitation of Unreal Engine 5 and not EOS.

!!!
In Unreal Engine 5, host migration can be handled in a few different ways. One common method is to designate one of the remaining clients as the new host. This client then takes over the responsibilities of the server, such as maintaining the game state and handling communication between players.

The process of host migration in Unreal Engine 5 involves several steps:

1. Detecting when the host has left the game or is otherwise unable to continue hosting[Handled by EIK].
2. Choosing a new host from the remaining clients.[Handled by EIK]
3. Transferring the game state to the new host. [Handled by EIK with the help of your game logic]
4. Updating all clients to communicate with the new host.[Handled by EIK]
5. Handling any issues that arise during the migration process, such as data loss or synchronization problems.[Handled by EIK]

### Proccess

Will be updated by 4th of January 2024.