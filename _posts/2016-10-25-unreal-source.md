---
layout: post
title:  "unreal source"
date:   2016-10-25 09:51:02
categories: unreal
---

## unreal

[Origin](https://docs.unrealengine.com/latest/INT/Programming/index.html)

#### Actors are instances of classes that derive from the AActor class;

#### Objects are instances of classes that inherit from the UObject class;

#### UObject:the base class of all objects in Unreal Engine, including Actors.

#### Actors can be thought of as whole items or entities, while Objects are more specialized parts.

#### gameplay classes such as GameMode, GameState, and PlayerState set the rules of the game

-------------------------

#### A Pawn is an Actor that can be an "agent" within the world.

#### A Character is a humanoid-style Pawn.

#### A Controller is an Actor that is responsible for directing a Pawn.

-------------------------
#### A HUD is a "heads-up display", or the 2D on-screen display that is common in many games.

#### The PlayerCameraManager is the "eyeball" for a player and manages how it behaves.

-------------------------
#### GameMode is the definition of the game, including things like the game rules and win conditions. It only exists on the server.

#### GameState contains the state of the game, which could include things like the list of connected players, the score

-------------------------
