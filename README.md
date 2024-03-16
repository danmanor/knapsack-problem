# Fantasy Basketball Roster Optimization Problem

This repository is dedicated to addressing the Fantasy Basketball Roster Optimization Problem, a complex mathematical challenge faced by fantasy basketball team managers. The goal is to maximize the number of games played by a team's players throughout a week, given a set of constraints.

## Problem Definition

In fantasy basketball, each team manager aims to optimize their player roster weekly to maximize the total games played. This involves strategic player substitutions under the league's rules and constraints. The problem is defined by the following key parameters and constraints:

### Parameters & Constraints

- **TEAM_PLAYER_SLOTS**: The number of active slots in a team.
- **TEAM_INJ_SLOTS**: Additional slots for players considered injured.
- **TEAM_SUBSTITUTION_LIMIT**: Maximum allowed substitutions in a week.
- **TEAM_ACTIVE_SLOTS**: The number of players that can be played each night out of the active roster.
- **TEAM_INTERCHANGEABLE_PLAYERS**: A specified subset of players that are eligible to be released from the team.

### Objective

3. **Game Maximization**: The objective is to maximize the total number of games played by the team's players during the week.

## Mathematical Formulation

The problem can be formulated as an integer programming model where the decision variables represent whether a player is active on a particular day, and the objective function maximizes the total number of player-games across the week. The constraints ensure adherence to the substitution limits and roster requirements.

### Variables

- Let `x_{i,d}` be a binary variable that represents whether player `i` is active on day `d`.

### Objective Function

- Maximize the sum of `x_{i,d}` across all players and days, weighted by the number of games each player plays on day `d`.

### Constraints

1. Sum of `x_{i,d}` for any day `d` must not exceed the number of active roster spots.
2. Total substitutions across the week must not exceed the allowed number.
3. Additional constraints to represent the subset of players eligible for release and injury considerations.

## Solution Approach

This repository implements a heuristic approach to solve the optimization problem, given its NP-hard nature. The algorithm iteratively evaluates potential roster configurations, making substitutions that are expected to yield the highest increase in the total number of games played, within the constraints.

## Contributing

Contributions to improve the algorithm or extend its functionality are welcome. Please feel free to fork the repository, make changes, and submit pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
