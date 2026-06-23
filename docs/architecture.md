# Architecture

## Philosophy

The project is built around a graph-first architecture.

Canonical lore data and user-created research data are intentionally separated.

This allows users to create notes, theories, groups, and investigations without modifying official data.

---

## System Architecture

Frontend
    ↓
API Layer
    ↓
Neo4j (Lore Graph)

PostgreSQL (User Data)

AI Service

Search Service

---

## Frontend

### Next.js

Responsibilities:

- Routing
- Authentication
- Workspace UI
- Graph UI

### Cytoscape.js

Responsibilities:

- Graph Rendering
- Node Layouts
- Clustering
- Group Visualizations
- Filtering

---

## Backend

### NestJS

Responsibilities:

- Authentication
- Workspace Management
- Note Management
- Theory Management
- Graph Queries

---

## Neo4j

Stores:

- Characters
- Events
- Locations
- Secrets
- Canon Relationships

Neo4j acts as the canonical source of truth.

---

## PostgreSQL

Stores:

- Users
- Notes
- Workspaces
- Custom Groups
- Theory Relationships
- Saved Views

---

## pgvector

Stores embeddings for:

- Semantic Search
- AI Analysis
- Similar Notes
- Lore Discovery