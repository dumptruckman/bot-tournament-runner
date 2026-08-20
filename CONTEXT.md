# Bot tournaments

This context describes autonomous players competing in game-defined contests and the administration of those contests.

## Language

**Bot**:
An autonomous player designed by a human to participate in a Match.
_Avoid_: Agent, AI, player process

**Bot Artifact**:
A prepared, identifiable executable representation of a Bot that can be started for a Match.
_Avoid_: Bot source, build

**Bot Instance**:
A fresh running instance created from a Bot Artifact for one Match. It carries no implicit state from other Matches.
_Avoid_: Bot Artifact, persistent Bot

**Match**:
One complete instance of a Game played by one or more Bots. A Match is the smallest unit of competitive execution.
_Avoid_: Game, round

**Match Plan**:
The immutable declaration of a Match before execution, including its Game, Bots, settings, seed, and limits. One Match Plan may have more than one execution attempt.
_Avoid_: Match Record, result

**Match Record**:
The immutable account of one attempt to execute a Match Plan, including observed interactions, diagnostics, and outcome.
_Avoid_: Match Plan, configuration

**Match Outcome**:
The Game-defined competitive result produced when any Match ends. It exposes normalized placements, including ties, for Tournament use and may include Game-specific summary data for display or audit.
_Avoid_: Final Match outcome, Tournament result

**Execution Fault**:
An objective runtime condition that prevented normal Bot interaction, such as a process exit, exceeded deadline, or protocol violation. The Game decides its competitive meaning.
_Avoid_: Forfeit, loss, Bot Failure

**Tournament**:
An administered competition that schedules Matches and determines results across them.
_Avoid_: Match, event

**Tournament Format**:
The policy a Tournament uses to schedule Matches and determine standings from normalized Match placements. Round-robin is the first supported Tournament Format.
_Avoid_: Game rules, bracket

**Game**:
The rules and interaction model that govern a Match.
_Avoid_: Match, tournament

**Observation**:
The Game-defined information presented to one Bot when the Game requests its next Action. Different Bots may receive different Observations of the same Game state.
_Avoid_: Game state, input

**Action**:
A Bot's Game-defined response to an Observation.
_Avoid_: Move, output
