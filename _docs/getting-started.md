---
title: Getting Started
tags: 
description: Getting started with DynamicGui
---

# Getting Started

## What you need to know

### Picking a configuration langauge


DynamicGui supports [yaml](https://learnxinyminutes.com/docs/yaml/), [json](https://learnxinyminutes.com/docs/json/), [hocon](https://github.com/lightbend/config#using-hocon-the-json-superset) and [xml](https://learnxinyminutes.com/docs/xml/)  for gui configuration. 
To write guis for DynamicGui you will need to know one the listed languages.

### Concepts

DynamicGui is broken down into a few different concepts

* Gui - Top level inventory, holds data about the inventory
* Slot - Inventories are made up of slots, hold the data for the icon of the slot, the lore etc
* Functions - Functions can be assigned to either guis or slots and are what perform various actions

### Gui

The gui is broken down into a few different basic parts:
* title - The title of the gui is the text that is displayed at the top of the inventory
* rows - The number of rows in the inventory, typically a max of 6 rows
* mode - The mode that the inventory should be built with
  * set - Set each slot at the given index, I.E: `0` is the first slot
  * add - Adds each slot to the inventory, this is useful if you run functions on build of the gui
* type
* //TODO - add types, locations, npcs, aliases etc maybe this should be added to another section

### Slot

Slots are the building blocks of guis, slots hold the items, function that are used for clicking on etc for the gui. 

Basic Slot properties:
* icon - The type of the icon that is displayed in the inventory - refer to the Javadocs for your specific spigot version
  * //TODO - Add links to Material Javadocs depending on spigot versions, maybe we should just host these ourselves on Github pages
* name (Optional) - The name of the item in the inventory
* data (Optional) - The damage or data value of the item in the inventory, exists for legacy support in versions < 1.13
* lore (Optional) - The lore of the item in the inventory
* functions (Optional) - The functions that will be ran from the slot, this will be explored more in the function section

### Function

//TODO - Functions