# Hexwar-Android-App

The Android menu and lobby screens for Hexwar, a multiplayer hex board game. This repo is the UI prototype. The game board and the networking were not built here.

## The problem

Hexwar was planned as a board game playable two ways: several players passing one phone around (hotseat), or each on their own device with one of them hosting. Before any game logic, that needs a flow of screens for choosing a mode, naming yourself, hosting and joining.

## What I built

Nine screens laid out in XML, each with its own activity.

| Screen | Purpose |
|---|---|
| Menu | Hotseat, Multiplayer, Settings |
| Hotseat | Player list for a shared-device game, with "Add player" |
| Multiplayer | Choose Join or Host |
| Host, Multiplayer hub | Lobby with the list of connected players |
| Join | List of available servers and a Connect button |
| Settings, Language, Name | Player name and language |

## State of the code

- Layouts are done. Navigation between them is not wired, so only the menu is reachable when you launch the app.
- There is no board, no game rules and no networking code. The Join screen's server list is a placeholder.

## Design decisions

- One activity per screen with ConstraintLayout, so each screen can be built and reviewed on its own.
- Buttons and backgrounds use shared shape drawables, so the look is defined once.
- Hotseat and network play use the same lobby pattern, a player list, since both end the same way: a list of players starting a game.

## Building

Android Gradle Plugin 7.0.2, Gradle 7.0.2, target SDK 30. Open it in Android Studio and accept the upgrade assistant, or build with JDK 11. No permissions or accounts needed.
