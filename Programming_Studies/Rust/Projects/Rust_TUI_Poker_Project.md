**What does the 'TUI-Klondike' written in Rust have that I can learn from?:**
- How to implement RNG using Rust
	- [[Rust-Card_RNG_Engine]]
- How to design the Terminal card 'Art'
	- [[Rust-TUI_Cards]]
- How to take key stroke inputs (Q, Arrow keys)
	- [[Rust-Interacting_With_a_TUI]]
- How are the card's values being stored?
	- [[Rust-Cardgame_Enum]]
- Define win con and what triggers when the game is over
	- [[Rust-Force_Exit_on_Condition]]

**What needs to be done?:**
- Create individual player's play areas & ask (ask if the player wants a table of 8 or 10)
- Find out the 'buy in' amount from the players
- Select a table to play at (Show open/taken seats)
- Create choices for Fold/Call/Check/Raise
- Show who's turn it is & start turn counter
- Deal out cards to each player
- Place down Flop/Turn/River
- Allow players to select & play w/ chip piles (fidget with chips) *note that the player's chips will be piled and others are just going to be a number.
- Define the win con & what happens once it's met
- What happens if a player disconnects/times out
- Playing remotely through SSH(maybe?) *note if so then implement SSH keys
- Server/Client based (More private) or single cluster w/ mult. clients (++Cost)
- Figure out anti-cheat (possibly by hashing the exact code that's being used by each client for the randomization of the deck of cards and if they don't match then that would mean the host possibly has a 'stacked' deck running).
- Implement this building scheme for regicide, Tarot, & Go
- Possibly host a kiwIRC for people wanting to host tables
- It would be cool to make some sort of automated virtual machines that host SSH servers for tables and make system users for the names of each person that is planning on sitting it at a table (The shell welcome script could just start the game and not allow any escaping the poker TUI game without killing the SSH session and subsiquently booting the person out !!! BE SURE TO ASK FIRST !!! but also allow the person to join back into the table without any repercussions)

---

[[RE_Rust_TUI_Klondike]]
[[Rust-Card_Game_Kanban]]
