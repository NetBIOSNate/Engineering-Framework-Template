# Adopt infrastructure that already serves consumers

## Goal

Bring existing assets under repeatable management while preserving identity, connectivity and recovery access.

1. Use read-only discovery to capture resource IDs, actual configuration, addresses, dependencies, state generation, owners and last change. Ask operators which exceptions keep older clients working. Sample from both the asset register and the running system to expose unmanaged equipment.
2. Choose one small ownership boundary. Record which controller writes each property, including inherited policies. Transfer one writer at a time. Separate provider-owned fields from project-managed fields before declaring desired state.
3. Model the observed object and preview adoption. Inspect inferred replacements, reordered lists, default encryption modes and generated names. Verify import preserves the original resource ID and critical configuration. Route a destructive replacement back for design review.
4. Document route preference, DNS caches, writer authority and telemetry labels for coexistence. Mirror read-only traffic where appropriate. If both sides accept writes, design deduplication or use a fenced cutover. Account for writes made after cutover when planning reversal.
5. Stage one controlled change, verify the consumer path, and confirm a second preview converges. Keep previous configuration and independent access until the reversal window closes. Give historical data, audit records and old contracts an owner.

A second operator should be able to identify the writer for each field, describe recovery after partial failure and reproduce the clean readback. Track inconsistent objects separately before expanding adoption.
