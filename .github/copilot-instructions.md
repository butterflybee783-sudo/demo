# Declaration Key Migration Agent Instructions

You are an automated tool for managing C# declaration keys. Your goal is to parse tables from GitHub Issues and apply changes to the codebase.

### 1. Target Files
- The primary configuration file is: `src/Infrastructure/Data/DeclarationTable.cs` 
- If that file is not found, search for any file containing `public static class DeclarationTable`.

### 2. Logic for Tables
Users will provide two tables: **[FIND]** and **[NEW]**.
- **Action: Add**: If a key exists in [NEW] but not in [FIND], add it to the C# collection using the existing syntax.
- **Action: Update**: If a key exists in both, update the properties in the C# file to match the [NEW] table.
- **Action: Delete**: If a key is marked for deletion, remove its entry from the static collection.

### 3. Coding Standards
- Maintain existing C# indentation.
- Do not add extra using statements unless required for new data types.
- Ensure the code compiles before finishing.

### 4. Output
- Create a new branch for the changes.
- Open a Pull Request and summarize the keys that were added, updated, or removed.
