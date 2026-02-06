# Instructions for Copilot Coding Agent
When assigned to a 'migration-request' issue:
1. **ADD**: Insert new rows into `DeclarationData.cs` using the 'ADD' table.
2. **UPDATE**: 
   - Use the `update_find_table` to locate the record in C#.
   - Use the `update_new_table` to get the new values.
   - Match them by row index (Row 1 of Find = Row 1 of New).
3. **DELETE**: Remove rows found in the 'DELETE' table.
4. **STYLE**: Maintain the existing C# static collection format.
