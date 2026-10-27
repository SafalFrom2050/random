# App Idea of the Day: Test Garden
Date: 2026-10-28 (Japan)

## Concept
A tiny simulator for testing an app against unreliable device telemetry. Define a few sensor fields, create a timeline of glitches, and stream repeatable test data to a development build over WebSocket.

## Target users
Mobile developers building dashboards for Bluetooth devices, hobby robots, environmental sensors, or other connected products.

## Problem
A physical device may be unavailable, and real hardware rarely reproduces the same failure twice. Happy-path mock data misses stale readings, missing fields, reconnects, and bursts of updates.

## Core workflow
1. Define a JSON message template, such as battery percentage, temperature, and sequence number.
2. Set a normal update interval and values.
3. Add timeline events: change a value, omit a field, pause messages, send malformed JSON, or close the connection.
4. Connect a development app through a small transport adapter.
5. Run the scenario and inspect timestamped messages.
6. Reset and replay the same scenario while checking the app's behavior.

Example: Send battery updates each second, stop for ten seconds, disconnect, then reconnect with a fresh snapshot to exercise stale-data and recovery screens.

## MVP features
- A local desktop interface for editing message templates.
- Deterministic timelines with explicit values and intervals.
- One WebSocket client at a time.
- Pause, resume, reset, and replay controls.
- An event log showing sent messages and connection changes.
- Scenario JSON import/export and a sample Flutter receiver.

This first version simulates an application-level message stream. It does not emulate BLE pairing, radio behavior, packet fragmentation, or a complete hardware protocol.

## Build approach
Build an Electron desktop app with a TypeScript scenario engine and a WebSocket server bound to loopback by default. Keep the engine independent of the interface so scenarios can later run from a command line.

Use a monotonic clock, an ordered event queue, and stable ordering for events with equal timestamps. Pause shifts future deadlines; reset clears all scheduled events and restores initial values. Reconnection is initiated by the client, and a scenario explicitly defines what to send after a new connection.

Validate scenario files before execution. Include engine tests for event ordering, pause/resume, disconnects, and cleanup between runs. The sample Flutter app demonstrates a swappable transport rather than requiring changes to production device code.

## Validation plan
Ask five developers with an existing connected-device UI to reproduce one known bug.
- Measure the time to connect their app and create the scenario.
- Check whether three replays reproduce the same message sequence.
- Observe whether the tool exposes a stale-data or reconnect issue their usual mocks miss.
- Ask participants to export a scenario and have another developer run it.
- Record which missing transport behavior prevents useful testing.

Continue if at least three developers independently create a useful scenario and reuse it during a fix. Narrow the scope if most need real BLE behavior before gaining value.

## Biggest risk
The simulator could be too far removed from the real device to reveal meaningful problems. Start with transport-independent telemetry screens, document the boundary clearly, and validate against an actual bug before building a general protocol editor.

## Possible business model
Offer the core local simulator free and explore paid team scenario libraries or automated replay reports after repeat use is established. Keep scenario files portable and readable.
