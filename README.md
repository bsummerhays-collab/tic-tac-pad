# Tic Tac Pad

Two-player tic tac toe you can play with someone over a link. No accounts, no server.

**Play:** https://bsummerhays-collab.github.io/tic-tac-pad/

## How it works

1. Open the page. You're X, and the page gives you an invite link.
2. Send the link to the other player. When they open it, they join as O.
3. Moves show up on both screens right away. Rounds alternate who opens, and the score carries over.

Every visit to the page starts its own game, so any number of games can run at once. Each game holds two players: anyone else who opens a game's invite link is told it's full and offered a new game of their own.

The two browsers connect directly to each other with WebRTC, using [PeerJS](https://peerjs.com/) and its free public server to set up the connection. The game state lives in the host's tab, so the host needs to keep that tab open. If the other player reloads, they rejoin the same game.

Everything is in `index.html`.
