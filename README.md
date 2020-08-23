---
description: >-
  This is the developer reference document for Catch.io. Developers starting
  this project should start from here.
---

# Introduction

## Document Structure

There are three groups; Scripts, Scenes, and Prefabs. Each of these groups represents a game resource category and within those categories, we divide them into subcategories \(namespaces or folder in the engine\).

* **Scripts** - everything about the game's script is stored in here. This generally means all \*.cs files that are inside `/Assets/Scripts/`
* **Scenes** - important game scenes that require an extra explanation for developers. This generally means all \*.unity files that are inside `/Assets/Scenes/`. Not every game scene needs to be documented!
* **Prefabs** - important prefabs used in the game. This generally means all \*.prefab files that are inside `/Assets/Resources/Prefabs/`. Not all prefabs will require documentation.

Documentation should match with the changes made to the `development/`branch of the project!

## Script Documentation Guide

Scripts are categorized by subfolders within the `Scripts` folder or namespaces. For example, the Player section refers to the player folder, not the `Player` class in the game.

Every class document should have a sub-document about their methods as well.

### Class Template

```text
# {class name}

## Description

{description of this class}

## Properties

| type | name | description |
| :--- | :--- | :--- |
| {type} | {property name} | {description} |

## Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| {type} | {method name} | {description} |
| {type} | {method name} | {description} |
```

### Method Template

```text
# {method name}

{method in script.
Example: `public static int DirectionToIndex(Vector2 dir, int sliceCount)`}

## Description

{method description}

## Children

| name | description |
| :--- | :--- |
| {name} | {prefab description} |
| {name} | {prefab description} |
```

## Scene Documentation Guide

Every major scene used in the game will be documented in this group. This generally refers to manager scenes, UI scenes, network lobby scenes, etc. Anything that is going to be added on to another scene, or entry scenes. Scene documentation should contain all the notable prefabs and their purpose in the scene.

### Template

```text
# {scene name}

## Description

{description of this scene}

## Prefabs/Objects

| prefab name | description |
| :--- | :--- |
| {prefab name} | {description} |
```

## Prefab Documentation Guide

Ever important prefab that is unique to this game will be documented in this group. These includes things like that camera manager, player prefab, game manager, etc.

### Template

```text
# {prefab name}

## Description

{description of this prefab}

## Prefabs/Objects

| prefab name | description |
| :--- | :--- |
| {prefab name} | {description} |
```

