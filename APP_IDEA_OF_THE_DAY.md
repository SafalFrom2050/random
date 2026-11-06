# App Idea of the Day: Cable Atlas
Date: 2026-11-07 (Japan)

## Concept
A visual notebook for remembering how a desk, home theater, or hobby electronics setup is connected. Photograph each cable's endpoints, give it a label, and create a simple connection map before unplugging anything.

## Target users
People moving desks, reorganizing home entertainment equipment, or maintaining small hobby electronics projects.

## Problem
After cleaning or moving equipment, similar-looking cables become difficult to reconnect. A wide photo rarely shows which port each cable used, and handwritten labels can lose their meaning.

## Core workflow
1. Create a setup such as “Living room TV.”
2. Add device cards with optional port names.
3. Photograph both ends of a cable and assign a short label, such as C03.
4. Record the connection: TV HDMI 2 → console HDMI output.
5. Print or handwrite matching labels for the physical cable.
6. Open a reconnect checklist after moving the equipment and confirm each connection manually.

Example: A desk map distinguishes the monitor's video cable from its USB hub cable, with close-up photos of the correct ports.

## MVP features
- Device and named-port records.
- Cable entries with endpoint photos and editable labels.
- A searchable connection list and simple device map.
- A reconnect checklist that can be reset for another move.
- Printable label sheets and offline access.
- ZIP backup export/import.

Record user-observed connections only. Automatic port recognition, electrical troubleshooting, compatibility guarantees, and network discovery are outside the first release.

## Build approach
Build a Flutter app with SQLite for setups, devices, ports, cables, and checklist sessions. Store photos locally and require no account.

Represent a cable as two explicitly chosen endpoints; allow an endpoint to remain unknown while documenting a setup. Use stable identifiers so renaming a device preserves its links. The map should support manual positioning, while the connection list remains the accessible alternative.

Starting a reconnect session snapshots the recorded connections so subsequent edits do not silently alter its checklist. Clearly distinguish “recorded” from “confirmed during this session”; neither means the app detected a working connection. Export a versioned JSON manifest with photos and validate referenced identifiers on import.

## Validation plan
Recruit eight people planning a desk or entertainment-system reorganization.
- Ask them to document five connections before unplugging equipment.
- Measure capture time and missing endpoint details.
- Observe whether they can locate the right port during reconnection.
- Compare their experience with their usual photos or labels.
- Check whether physical labels remain readable and useful.
- Verify backup restoration on a second device.

Continue if five participants voluntarily document another setup and can identify a connection detail the notebook helped them recover. Treat this as evidence of retrieval usefulness, not proof of fewer hardware faults.

## Biggest risk
Documenting both endpoints may feel too slow, and incomplete records could be misleading. Make a cable label and one photo sufficient for a draft, highlight unknown endpoints, and test capture effort on actual cramped desks before adding more map features.

## Possible business model
Free for one setup, with a one-time upgrade for unlimited setups and custom label layouts. Keep basic backup and the connection list available to everyone.
