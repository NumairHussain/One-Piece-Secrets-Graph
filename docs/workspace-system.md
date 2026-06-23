# Workspace System

## Purpose

Workspaces transform the application from a graph explorer into a research platform.

A workspace is a saved investigative environment.

Users can build theories, research topics, save notes, and organize information without affecting the canonical graph.

---

# Core Philosophy

The graph represents the world.

The workspace represents the user's understanding of the world.

---

# Workspace Components

Each workspace may contain:

* Filters
* Saved layouts
* Notes
* Theory relationships
* Timeline position
* Camera position
* Selected nodes
* Hidden nodes
* AI reports
* Custom groups

---

# Workspace Types

## Private Workspace

Accessible only by the owner.

---

## Shared Workspace

Shared through URL.

Read-only or collaborative.

---

## Community Workspace

Future feature.

Public investigations visible to all users.

---

# Workspace Snapshots

Users can freeze workspace state.

Snapshots preserve:

* Notes
* Timeline state
* Filters
* Theories
* Layouts

Useful for preserving research history.

---

# Workspace Groups

Users can create custom visual groups.

Examples:

* D Clan Members
* God Valley Participants
* Joy Boy Researchers
* Ohara Survivors

Groups are visualization tools only.

---

# Sharing

Users can share:

* Entire workspaces
* Snapshots
* Individual investigations
* AI reports

---

# Future Collaboration

Future collaborative features may include:

* Multiple editors
* Comment threads
* Shared notes
* Shared theory boards
* Research teams

---

# Storage Model

Workspaces are stored in PostgreSQL.

Canonical graph data remains in Neo4j.

Workspaces reference graph entities but never modify them.
