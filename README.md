# One Piece Secrets Graph

A core design principle of this project is that the graph should never force a single interpretation of the data.

Every user explores One Piece differently.

Some users care about crews.

Some care about lore.

Some care about individual characters.

Some want a clean graph.

Others want every possible connection visible.

### A User-Controlled Visualization Philosophy

Because of this, nearly every visual component should be configurable from the frontend.

The application should feel less like a static website and more like a personal investigation board that users can customize to match how they think.

---

# Custom Graph Controls

The frontend should provide a powerful control panel that allows users to modify the graph in real-time.

Users should be able to:

- Show or hide group boundaries
- Show or hide relationship lines
- Show or hide specific categories of nodes
- Change graph density
- Change clustering behavior
- Highlight important secrets
- Focus on specific story arcs
- Save custom graph layouts
- Create custom filters
- Create custom groups

Changes should happen instantly without reloading the graph.

---

# Grouping Controls

Groupings are intended to provide context, not restrictions.

By default, official groups may exist for:

- Straw Hat Pirates
- Roger Pirates
- Heart Pirates
- Kid Pirates
- Marines
- Revolutionary Army
- World Government
- Yonko Crews
- Warlords
- Individual Kingdoms

However, users should be able to completely control how groups are displayed.

Options include:

### Show Group Boundaries

Display visual outlines around related nodes.

Example:

A circular outline around the Straw Hat Pirates.

### Hide Group Boundaries

Remove all outlines and display only nodes and connections.

### Highlight Groups

Make selected groups visually stand out.

### Dim Unselected Groups

Reduce visual noise by fading unrelated groups.

---

# User-Created Groups

Users should not be limited to predefined groups.

They should be able to create their own custom collections.

Examples:

### Characters Who Know About Joy Boy

- Nico Robin
- Vegapunk
- Rayleigh
- Roger
- Oden

### Survivors of Ohara

### Members of the D Clan

### Characters Present at God Valley

### Personal Theory Groups

Users could even create groups based on their own theories and interpretations.

These groups should exist purely as visualization tools and should not modify the underlying data.

---

# Crew Filtering

Users should be able to isolate entire crews with a single click.

Examples:

- Show only Straw Hat Pirates
- Show only Heart Pirates
- Show only Roger Pirates
- Show only Blackbeard Pirates

When enabled, the graph focuses on those crews and their connected secrets.

---

# Character-Level Filtering

Users should not be forced to view an entire crew.

Individual characters should be selectable.

Examples:

Show only:

- Nico Robin
- Trafalgar Law
- Dr. Vegapunk

Or:

- Nico Robin
- Rayleigh
- Saul
- Vegapunk

Even if those characters belong to completely different organizations.

This allows users to investigate specific theories, relationships, and information pathways across the entire world.

---

# Multi-Character Comparison Mode

Users should be able to manually select any collection of characters and compare them together.

Examples:

Compare:

- Robin
- Law
- Vegapunk

Or:

- Roger
- Rayleigh
- Oden

Or:

- Blackbeard
- Shanks
- Dragon

The graph updates to show only relevant relationships and shared secrets.

This creates a powerful lore-analysis tool.

---

# Secret-Centric Mode

Instead of focusing on characters, users can focus on a specific mystery.

Examples:

### Joy Boy Mode

Show:

- Every connected character
- Every related event
- Every related location
- Every related artifact

### Void Century Mode

### Ancient Weapons Mode

### Will of D. Mode

The selected secret becomes the center of the graph.

Everything else reorganizes around it.

---

# Arc and Timeline Controls

Users should be able to filter the graph by story progression.

Examples:

- East Blue
- Alabasta
- Skypiea
- Water 7
- Enies Lobby
- Marineford
- Dressrosa
- Whole Cake Island
- Wano
- Egghead

This allows users to examine how knowledge evolved during specific periods of the story.

---

# Custom Views

Users should be able to save their own graph configurations.

Examples:

"My Void Century Research"

"My Robin Investigation"

"Characters Connected To Joy Boy"

"Marine Knowledge Network"

Saved views can be reopened later without rebuilding the filter set.

---

# AI Analysis Controls

AI features should always be optional.

Some users may want a purely visual experience.

Others may want analytical assistance.

The user should be able to:

- Enable AI Analysis
- Disable AI Analysis
- Hide AI-generated insights
- Generate custom reports
- Compare selected characters
- Analyze selected groups
- Analyze selected secrets

The graph should remain fully functional even if AI features are completely disabled.

---

# Advanced Investigation Mode

An optional mode for power users.

This mode allows users to build highly specific investigations.

Examples:

Show:

- Nico Robin
- Vegapunk
- Ohara
- Joy Boy

Hide:

- Everyone else

Or:

Show:

- All members of the Roger Pirates
- All Road Poneglyphs
- Laugh Tale

Hide:

- Everything unrelated

The result is a focused research workspace tailored to the user's interests.

---

# Ultimate Goal

The application should not dictate how users explore One Piece.

Instead, it should provide a flexible investigative sandbox where users can:

- Explore the story visually
- Follow knowledge pathways
- Compare characters
- Create custom groups
- Build custom theories
- Save custom investigations
- Analyze mysteries
- Control exactly what appears on screen

Every user should be able to create their own version of the One Piece knowledge graph without changing the underlying data.