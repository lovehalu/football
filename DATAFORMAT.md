# Match Statistics Data Structure

## Overview
This document defines the data structure for collecting detailed match statistics. The aim is to keep track of critical events during a football match, which includes goals, corners, yellow cards, and red cards.

## Data Structure

```json
{
  "matchId": "string",
  "teamA": {
    "name": "string",
    "goals": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "corners": [
      {
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "yellowCards": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "redCards": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ]
  },
  "teamB": {
    "name": "string",
    "goals": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "corners": [
      {
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "yellowCards": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ],
    "redCards": [
      {
        "playerId": "string",
        "time": "string"  // Format: HH:MM:SS
      }
    ]
  }
}
```

## Fields Description
- **matchId**: Unique identifier for the match.
- **teamA** / **teamB**: Objects containing the team's statistics. 
- **name**: The name of the team.
- **goals**: Array of goals scored by the team, each including the player's ID and time of the goal.
- **corners**: Array of corner kicks, including the time of the corner.
- **yellowCards**: Array of yellow cards received, including the player's ID and time.
- **redCards**: Array of red cards received, including the player's ID and time.

## Example
```json
{
  "matchId": "12345",
  "teamA": {
    "name": "Team Alpha",
    "goals": [{"playerId": "123", "time": "00:15:30"}],
    "corners": [{"time": "00:16:45"}],
    "yellowCards": [{"playerId": "124", "time": "00:20:00"}],
    "redCards": []
  },
  "teamB": {
    "name": "Team Beta",
    "goals": [{"playerId": "223", "time": "00:30:00"}],
    "corners": [{"time": "00:31:20"}],
    "yellowCards": [],
    "redCards": [{"playerId": "224", "time": "00:40:00"}]
  }
}
```
