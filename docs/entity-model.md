# Entity Model

## Purpose

The Entity Model defines every canonical object that may exist within the One Piece Secrets Graph.

This document serves as the single source of truth for:

* Node Types
* Relationship Types
* Timeline Fields
* Validation Rules
* Visualization Rules
* AI Context Rules
* Future Expansion

Every service in the system should reference this document.

---

# Core Philosophy

Canonical entities represent information that exists within the story.

User theories, notes, and custom relationships are stored separately within Workspaces.

---

# Universal Entity Structure

Every graph entity inherits the following fields.

```typescript
interface GraphEntity {
  id: string;
  type: EntityType;

  name: string;
  description?: string;

  firstChapter?: number;
  firstEpisode?: number;

  imageUrl?: string;

  createdAt: Date;
  updatedAt: Date;
}
```

---

# Entity Types

All entity types will be a circle just different colored

## Character

Represents an individual person.

Examples:

* Monkey D. Luffy
* Nico Robin
* Trafalgar Law
* Dr. Vegapunk
* Gol D. Roger

### Properties

```typescript
{
  type: "character";

  aliases?: string[];

  status?: string;

  bounty?: number;

  affiliations?: string[];

  titles?: string[];
}
```

### Visual Representation

Shape:

Circle

---

## Organization

Represents a formal group.

Examples:

* Straw Hat Pirates
* Marines
* Revolutionary Army
* World Government

### Properties

```typescript
{
  type: "organization";

  category:
    | "crew"
    | "government"
    | "military"
    | "kingdom"
    | "other";
}
```

### Visual Representation

Shape:

Hexagon

---

## Location

Represents a place.

Examples:

* Ohara
* Wano
* Egghead
* Elbaf
* Laugh Tale

### Properties

```typescript
{
  type: "location";

  sea?: string;

  region?: string;
}
```

### Visual Representation

Shape:

Location Marker

---

## Event

Represents a major occurrence.

Examples:

* Marineford War
* God Valley Incident
* Ohara Incident

### Properties

```typescript
{
  type: "event";

  startChapter?: number;

  endChapter?: number;

  arc?: string;
}
```

### Visual Representation

Shape:

Diamond

---

## Secret

Represents hidden information.

Examples:

* Joy Boy
* Void Century
* Will of D.
* Ancient Kingdom

### Visual Representation

Shape:

Star

These should be among the most visually prominent nodes.

---

## Artifact

Represents important objects.

Examples:

* Road Poneglyph
* Ancient Weapons
* Giant Straw Hat

### Properties

```typescript
{
  type: "artifact";
}
```

### Visual Representation

Shape:

Square

---

## Concept

Represents abstract ideas.

Examples:

* Freedom
* Inherited Will
* Dreams

### Properties

```typescript
{
  type: "concept";
}
```

### Visual Representation

Shape:

Rounded Rectangle

---

# Relationship Model

All relationships inherit the following structure.

```typescript
interface GraphRelationship {
  id: string;

  sourceId: string;
  targetId: string;

  relationshipType: RelationshipType;

  chapter?: number;
  episode?: number;

  confidence?: number;
}
```

---

# Relationship Types

## KNOWS

Character possesses knowledge.

Example:

Robin → KNOWS → Joy Boy

---

## LEARNED_ABOUT

Represents a specific learning event.

Example:

Robin → LEARNED_ABOUT → Void Century

---

## BELONGS_TO

Membership.

Example:

Robin → BELONGS_TO → Straw Hat Pirates

---

## VISITED

Travel relationship.

Example:

Roger → VISITED → Laugh Tale

---

## PARTICIPATED_IN

Participation.

Example:

Garp → PARTICIPATED_IN → God Valley Incident

---

## DISCOVERED

Discovery.

Example:

Robin → DISCOVERED → Poneglyph Information

---

## RELATED_TO

General lore connection.

Example:

Void Century → RELATED_TO → Ancient Kingdom

---

## LOCATED_AT

Location association.

Example:

Road Poneglyph → LOCATED_AT → Zou

---

## INHERITED_FROM

Inheritance of will or information.

Example:

Luffy → INHERITED_FROM → Roger

---

# Timeline Fields

Timeline progression is a core feature.

Every entity may contain:

```typescript
{
  firstChapter?: number;

  firstEpisode?: number;
}
```

Every relationship may contain:

```typescript
{
  chapter?: number;

  episode?: number;
}
```

These values determine visibility.

Example:

If user selects Chapter 500:

Show:

Relationships <= 500

Hide:

Relationships > 500

---

# Visibility Rules

Visibility is determined by:

## Timeline

Chapter/Episode progress.

---

## Workspace Settings

User preferences.

---

## Layer Settings

* Canon
* Notes
* Theories
* AI
* Community

---

# Validation Rules

## Canon Graph

Must contain:

* Valid source
* Valid target
* Valid relationship type

---

## Timeline Integrity

Relationship chapter cannot occur before source entity introduction.

Invalid:

Robin learns secret in Chapter 50.

Robin first appears in Chapter 114.

---

## Entity Uniqueness

Every canonical entity must be unique.

Allowed:

One Joy Boy node.

Not Allowed:

Multiple Joy Boy nodes.

---

# Visual Group Rules

Groups are overlays.

Groups never create relationships.

Example:

Straw Hat Pirates boundary.

Inside:

* Luffy
* Zoro
* Robin

Joy Boy may only connect to Robin.

No automatic propagation occurs.

---

# AI Rules

AI may:

* Explain entities
* Explain relationships
* Generate summaries
* Discover patterns

AI may not:

* Modify canonical graph
* Create canonical relationships
* Override human validation

---

# Future Expansion

The Entity Model is universe-agnostic.

Future implementations may support:

* Black Ops Zombies
* Star Wars
* Attack on Titan
* Lord of the Rings
* Game of Thrones

Only entity definitions and relationship definitions would need to change.

The graph engine itself remains unchanged.
