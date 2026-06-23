# Data Model

## Overview

The application uses a hybrid storage model.

### Neo4j

Stores canonical graph data.

### PostgreSQL

Stores user-generated data.

---

# Neo4j Models

## Character

```json
{
  "id": "character_001",
  "name": "Nico Robin",
  "type": "character",
  "firstChapter": 114,
  "firstEpisode": 67
}
```

---

## Secret

```json
{
  "id": "secret_001",
  "name": "Joy Boy",
  "type": "secret"
}
```

---

## Event

```json
{
  "id": "event_001",
  "name": "God Valley Incident",
  "type": "event"
}
```

---

## Location

```json
{
  "id": "location_001",
  "name": "Ohara",
  "type": "location"
}
```

---

## Relationship Model

```json
{
  "sourceId": "character_001",
  "targetId": "secret_001",
  "relationship": "KNOWS",
  "chapter": 628,
  "episode": 548
}
```

---

# PostgreSQL Models

## User

```sql
users
```

Fields:

* id
* username
* email
* created_at

---

## Workspace

```sql
workspaces
```

Fields:

* id
* user_id
* name
* description
* created_at
* updated_at

---

## Workspace Snapshot

```sql
workspace_snapshots
```

Fields:

* id
* workspace_id
* snapshot_name
* created_at

---

## Note

```sql
notes
```

Fields:

* id
* workspace_id
* title
* content
* note_type
* created_at
* updated_at

---

## Note References

```sql
note_references
```

Fields:

* note_id
* entity_id
* entity_type

---

## Custom Groups

```sql
custom_groups
```

Fields:

* id
* workspace_id
* name

---

## Custom Group Members

```sql
custom_group_members
```

Fields:

* group_id
* entity_id

---

## Theory Relationships

```sql
theory_relationships
```

Fields:

* id
* workspace_id
* source_entity
* target_entity
* relationship_name
* evidence
* confidence

---

## Saved Views

```sql
saved_views
```

Fields:

* id
* workspace_id
* name
* layout_state
* filter_state
* timeline_state

---

# Future Models

## Collaboration

* workspace_members
* workspace_permissions

---

## Comments

* comments
* comment_threads

---

## AI Reports

* ai_reports
* ai_report_snapshots

---

# Separation of Concerns

Neo4j owns:

* Canonical nodes
* Canonical relationships
* Timeline data

PostgreSQL owns:

* Users
* Workspaces
* Notes
* Theories
* Groups
* Saved views
* AI reports

This separation ensures user-generated content never modifies the canonical One Piece graph.