# One Piece Secrets Graph: Project Overview

## What is it?
The One Piece Secrets Graph is an Obsidian-inspired visual knowledge graph for exploring the lore, characters, and mysteries of the One Piece universe. Instead of a traditional wiki, it maps out how information, secrets, and events connect across the story.

## Core Philosophy
The project strictly separates **Canonical Lore** (verified facts from the story) from **User Theories** (personal notes and custom relationships). The graph represents the world, while the workspace represents the user's understanding of it.

## Architecture & Services
The system utilizes a hybrid storage architecture to maintain the separation of canon and user data.

### Frontend
* **Next.js & React:** Handles routing, authentication, and the overall UI.
* **Cytoscape.js:** Powers the interactive graph rendering, node layouts, and visual clustering.

### Backend Services
* **NestJS:** Manages user authentication, workspaces, notes, and executes graph queries.
* **AI Service (OpenAI):** Provides optional graph summaries, relationship explanations, and lore insights.

### Databases
* **Neo4j (The Canon):** The graph database that acts as the single source of truth. It stores all canonical Characters, Events, Locations, Secrets, and their Canon Relationships.
* **PostgreSQL (The Sandbox):** A relational database that stores all user-generated content, including Users, Workspaces, Notes, Custom Groups, and Theory Relationships.
* **pgvector:** Stores embeddings for semantic search, similar notes discovery, and AI analysis.

## Key Features
* **Interactive Graph:** The primary experience. Users can pan, zoom, filter, and explore the connections of the One Piece world.
* **Timeline System:** Users can set their current chapter/episode progress to dynamically hide future events and relationships, ensuring spoiler protection.
* **Research Workspaces:** Personal environments where users can save layout states, apply custom filters, and build their own theory relationships without altering the main official graph.
* **Notes System:** Users can write markdown notes and attach them directly to specific characters, relationships, or keep them as standalone research journals.
* **Custom Groups:** Visual boundary overlays to group entities (e.g., "Ohara Survivors") for organizational purposes.

## The Entity Model
Everything in the application exists as Nodes and Relationships.
* **Nodes:** Represent entities like Characters, Organizations, Locations, Events, Secrets, and Artifacts.
* **Relationships:** Define how nodes connect functionally and temporally (e.g., *KNOWS*, *LEARNED_ABOUT*, *VISITED*, *PARTICIPATED_IN*, *BELONGS_TO*).