# Graph System

## Purpose

The Graph System is the core of One Piece Secrets Graph.

Everything in the application ultimately exists as nodes and relationships.

The graph represents the canonical world of One Piece and serves as the foundation for:

* Exploration
* Timeline analysis
* Notes
* Workspaces
* AI analysis
* Theory creation

The graph is intentionally designed to resemble an Obsidian Graph View while supporting significantly richer relationships and filtering capabilities.

---

# Design Principles

## Graph First

The graph is the primary user experience.

All other systems exist to enhance graph exploration.

---

## Canon First

The canonical graph represents verified One Piece information.

User-generated content never modifies the canonical graph.

Instead, user content exists as overlays.

---

## Fully Filterable

Every visual element should be filterable.

Users should control:

* Nodes
* Relationships
* Groups
* Layers
* Timeline visibility
* Notes visibility
* Theory visibility

---

# Node Types

## Character

Represents individual people.

Examples:

* Monkey D. Luffy
* Nico Robin
* Trafalgar Law
* Dr. Vegapunk

---

## Organization

Represents groups and institutions.

Examples:

* Straw Hat Pirates
* Marines
* Revolutionary Army
* World Government

---

## Location

Represents physical places.

Examples:

* Ohara
* Wano
* Egghead
* Laugh Tale

---

## Event

Represents significant moments.

Examples:

* God Valley Incident
* Marineford War
* Ohara Incident

---

## Secret

Represents lore concepts.

Examples:

* Joy Boy
* Void Century
* Will of D.
* Ancient Kingdom

---

## Artifact

Represents objects of significance.

Examples:

* Road Poneglyph
* Ancient Weapons
* Giant Straw Hat

---

# Relationship Types

## KNOWS

Character possesses knowledge about a secret.

Robin → KNOWS → Joy Boy

---

## LEARNED_ABOUT

Represents the moment information was acquired.

Robin → LEARNED_ABOUT → Void Century

---

## VISITED

Character visited location.

Roger → VISITED → Laugh Tale

---

## PARTICIPATED_IN

Character participated in event.

Garp → PARTICIPATED_IN → God Valley Incident

---

## BELONGS_TO

Membership relationship.

Robin → BELONGS_TO → Straw Hat Pirates

---

## RELATED_TO

Generic lore connection.

Void Century → RELATED_TO → Ancient Kingdom

---

## DISCOVERED

Discovery relationship.

Robin → DISCOVERED → Poneglyph Information

---

# Visual Representation

## Character Nodes

Circular nodes.

---

## Secret Nodes

Highlighted nodes.

Secrets should visually stand out from ordinary nodes.

---

## Event Nodes

Diamond-shaped nodes.

---

## Location Nodes

Location-style markers.

---

## Artifact Nodes

Square nodes.

---

# Grouping System

Groups are visual overlays.

Groups never imply shared knowledge.

Example:

The Straw Hat Pirates may appear inside a circular boundary.

Only Robin may connect to Joy Boy.

The existence of a group does not automatically create relationships.

---

# Graph Views

## Dynamic Graph View

Default experience.

Obsidian-style graph.

---

## Bipartite View

Characters and organizations on one side.

Secrets on the other.

---

## Matrix View

Character-to-secret comparison grid.

---

# Filtering

Users may filter by:

* Character
* Organization
* Secret
* Event
* Location
* Timeline
* Layer
* Notes
* Workspaces

---

# Performance Goals

Target:

* Thousands of nodes
* Thousands of relationships
* 60 FPS interactions
* Real-time filtering
* Instant node expansion
* Client-side graph manipulation
