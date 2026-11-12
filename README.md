# Sparta Tic-Tac-Toe

A browser-based Tic-Tac-Toe game with a Node.js 20 backend, a scoring system, an escalating computer opponent, and a top-10 scoreboard. Scores can live in the browser, in server memory, or in MongoDB, depending on how you configure it.

The server is built on Node's built-in http module (no Express), with structured logging via pino and Prometheus metrics via prom-client.

### Features
- Play as X against the computer (O) on a 3×3 board.
- Escalating difficulty by round
- Scoring: each win is worth 100 points. Draws add 100 points to a carry-over bonus that is paid out on your next win. A loss ends the run and resets the carry.
- Top-10 scoreboard: when a run ends, enter 3-letter initials to submit your score.
- Three storage modes (see below), chosen automatically from environment variables.
- Optional custom marker images (x.png / o.png) in place of text X and O.
- Observability: JSON logs with correlation IDs and a /metrics endpoint.

### Requirements
**Node.js** 20 or later
**MongoDB** (optional, only for the persistent mode)

test webhook is working on main branch
test dev 2.0