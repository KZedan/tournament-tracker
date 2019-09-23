# Tournament Tracker
A Tournament Tracker App designed in C#

# Scenario
Your friends come to you and ask you to create a tournament tracker. They are always playing games and want to determine who is the best. RThe idea is that you create a bracket tournament system where the computer will tell them who to play in a single-elimination style bracket. At the end, the winner should be identified. Their model is the NCAA basketball tournament bracket for March Madness.

# Requirements
1. Tracks games played and their outcome (who won).
2. Multiple competitors play in the tournament.
3. Creates a tournament plan (who plays in what order).
4. Schedules games.
5. A single loss eliminates a player.
6. The last player standing is the winner. 

# Structure
* A Windows Forms application and Class Library.
* SQL and/or Text File
* Users are one at a time on one application.

# Key Concepts
* Email
* SQL
* Custom Events

# Data Mapping
### Team
* Team Members (List<Person>)
* Team Name (string)

### Person
* FirstName (string)
* LastName (string)
* EmailAddress (string)
* PhoneNumber (string)

### Tournament
* TournamentName (string)
* EntryFee (decimal)
* EnteredTeams (List<Team>)
* Prizes (List<Prize>)
* Rounds (List<List<Matchup>>)

### Prize
* PlaceNumber (int)
* PlaceName (string)
* PrizeAmount (decimal)
* PrizePercentage (double)

### Matchup
* Entries (List<MatchupEntry>)
* Winner (Team)
* MatchupRound (int)
  
### MatchupEntry
* TeamCompeting (Team)
* Score (double)
* ParentMatchup (Matchup)
