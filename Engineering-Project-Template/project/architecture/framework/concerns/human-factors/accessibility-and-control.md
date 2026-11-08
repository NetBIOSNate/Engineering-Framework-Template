# Design human authority, accessibility and handoff

Whenever a design relies on a person, treat the interaction as an architectural interface. Identify the person's authority, what information they can perceive, the time available to act and the feedback that confirms the outcome. Include occasional users, maintainers and the incoming shift.

## Walk a time-critical task

1. Select a task whose failure changes the mission. Ask a representative user to show how it is done in the actual context, including noise, gloves, fatigue, low bandwidth, assistive technology or limited access where relevant.
2. Map each decision to the information available at that moment. Show actual state, age, uncertainty and source. Separate a requested change from its confirmed effect.
3. Identify what the user can undo and what requires additional authority. Make consequential commands distinguishable and give the operator a recovery route after a partial action.
4. Choose a task-level acceptance measure with the user owner. Record assistance needed, errors, completion time and whether users can recover without a designer coaching them.

## Example of an unreliable handoff

A returning operator sees green next to a pump symbol after the monitoring link has failed. The color came from a cached “running” value. The architectural requirement is to expose freshness, source and control authority through the status contract. The presentation can then convey “last confirmed running, 14 minutes ago” with more than one perceptible cue. Define what commands remain available when the state is unknown and who authorizes intervention.

For a digital workflow, exercise the whole critical task with keyboard navigation, assistive technology and textual feedback relevant to the users. For equipment, check reach, labels, force, visibility and the physical environment with a representative user. Record where a specialist assessment or formal acceptance criterion applies to the actual product.

Ask the receiving shift to explain unresolved work and outstanding authority from the handoff record alone. If staff must memorize hidden state or reconstruct it from several clocks, assign the missing information to a system component or procedure. Link the [mode and authority table](../../../system-context/framing/operating-environment/modes-and-authority.md).

[Architecture field guide](../../README.md)
