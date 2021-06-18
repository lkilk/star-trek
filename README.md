# Star Trek

This repo contains a simulator that is used to train new Star Fleet captains. It's playable in the terminal and it's great fun but, sadly, you are not destined for captainhood!  Star Fleet needs your skills elsewhere, in the software engineering team.

## Your Job

The simulator has worked well for many years but as our explorations continue and the Federation has evolved, some updates are required.

A new ally has been made in the Betazoids, so they need to be represented in the simulator. Also, the federation now applies a tax to propulsion fuel but we can reclaim it later on – we just need to keep accurate records. We'd also appreciate it if you could leave the codebase in a better state than it is now!

### Testing
There are no tests! It would be great if you could add some.

### Refactoring
The codebase is messy and hard to understand. Survey it for problems and get it into shape.

### Betazoids

- Are placed in one random quadrant
- Their ship is discoverable in the same way as you discover enemies
- Their weapons and other systems are the same as ours, since we now collaborate on ship design
- Betazoids assist the Enterprise in combat if within range of both the Enterprise and the enemy

### Fuel Tax
- Each journey we make between star bases should be logged
- Details should include distance travelled and fuel consumption
- Each time we refuel, the amount of fuel and the starbase obtained should be logged

## Development History

Originally written in 1979 for COBOL on Multics, by Kurt Wilhelm.

It was ported to OpenCOBOL 1.1 by Harald Arnesen in 2010.

Brian Tiffin updated the code, a little, removing comp-5 to fix some
random number generator byte ordering issues and to add new build
instructions.  This code requires a special configuration setting of

    perform-osvs:yes

This allows for overlapping exit points when combining GO TO and paragraph
THRU performs. The code also requires -free or a

    text-width:132

setting, as it contains long source lines.

## Game Objective

Star fleet is under attack from a Klingon invasion force.

Your job is too clear space around Federation HQ.

## Captain's Orders

Commands include

- nav, Navigate. Prompts for direction and warp factor.
  Command can be shortened to navdw
  for example: nav13 for direction 1, warp speed 3.

- pha, Phasers.  Prompts for power level from 300 to 9999
  dependent on current fuel levels.

- tor, Torpedo.  Fires a photon torpedo.

- def, Shields.  Prompts for shield power level
  dependent on available fuel.

- doc, Dock.     Attempt to dock the ship at a nearby star base
  for refueling and repairs.

- com, Computer. Starts up the computer with six available functions.
  Command can be shortend to comc, for example com3.

  - 1, requests ship status report.
  - 2, requests a short range scan of current quadrant.
  - 3, requests a long range scan.  Quadrants are numbered by column,row.
  - 4, requests a Klingon tally.
  - 5, requests an intelligence report.
  - 6, to abandon ship.
  - invalid function code will ask if assistance is required
    answer "yes" for a list of computer functions.

- invalid commands with cause a prompt asking if assistance is required,
  answer "yes" for a list of valid commands.

## Navigation

Directions are plotted with
```
    1
  8   2
7  -x-  3
  6   4
    5
```
Local space is a 9 by 9 grid of quadrants, numbered by column and then row.

Good luck, Captain.  Be wary the Romulans.
# star-trek
