# Inheritance Arena RPG

## Features

* **Base Character Class:** Created a parent `Character` class with auto-properties (`Name`, `Health`, `MaxHealth`, `AttackPower`), a computed property (`IsAlive => Health > 0`), and a `protected` constructor.
* **Subclasses & Unique Mechanics:** Implemented derived hero and monster classes (`Warrior`, `Mage`, `Goblin`, `Dragon`) with specialized combat logic:
  * **Warrior:** Reduces incoming damage using a `ShieldBlock` property and `Math.Max`.
  * **Mage:** Manages a `Mana` pool to cast high-damage Fireballs or fall back to a weak staff attack.
  * **Goblin:** Uses `Random.Shared.Next` to trigger a 30% chance for a bonus second strike.
* **Enemy Queue System:** Utilized a generic `Queue<Character>` collection to manage sequential dungeon encounters (`Enqueue`, `Peek`, `Dequeue`).
* **Interactive Combat Loop:** Built nested `while` loops to handle real-time turn-based combat, user console input, and win/loss game states.

## What I learned in this project

* **Inheritance (`:` and `base`):** How to share common properties and methods across multiple subclasses and pass data to a parent constructor using `: base(...)`.
* **Polymorphism (`virtual` & `override`):** How to define default or empty methods in a base class and override them in subclasses so each character type executes unique attack and defense behaviors.
* **Access Modifiers (`public` vs `protected`):** How `protected` restricts direct instantiation of the base `Character` class while still allowing derived classes to initialize their inherited stats.
* **Properties & Expressions:** How auto-properties (`{ get; set; }`) control data access and how expression-bodied properties (`=>`) dynamically calculate states on the fly.
* **Queue Collection (FIFO):** How to store different subclass objects inside a single `Queue<Character>` collection and process them in a First-In, First-Out order during combat.
