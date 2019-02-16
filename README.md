# Elo Chess Ranking API

_Note that this is not a full fledged API meant to be used elsewhere. This was just an hour of messing around_

Use the Elo module for the Elo Ranking System.
The Elo module is implemented using static methods so it should be called as "Elo._funcname_()"

# Quick-Start
## Creating the Elo ranking system
### 1. Import the API
```
from Elo import Elo
```
### 2. Initialize Elo
```
Elo.init()
```

## Using the Elo module
### Add Players
To add a player, you need to specify a player id. Optionally, you can also add a player rating but it defaults to 1200 if you dont.
```
Elo.add_player(player_id[, rating=1200])
```
### Remove Players
To remove a player, you need to specify a player id.
```
Elo.remove_player(player_id)
```
### Get Player
To get a player, you need to specify the player id
```
Elo.get_player(player_id)
```
### Display All Players
```
Elo.disp_players()
```

### Add Match
To add a match, you need to specify two players. A match id will be generated for the newly created match.
```
Elo.add_match(playerA, playerB)
```
### End Match
Ending a match takes the match id and scores earned by the players as a "MatchOutcomes" type. Import MatchOutcomes and use either MatchOutcomes.win, MatchOutcomes.lose, or MatchOutcomes.draw. This also updates the ratings of the players.
```
Elo.end_match(match_id, score_a, score_b)
```
### Display All Matches
```
Elo.disp_matches()
```
### Get number of matches
```
Elo.get_match_count()
```
