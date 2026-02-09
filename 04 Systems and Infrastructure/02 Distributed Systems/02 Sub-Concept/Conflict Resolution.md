# Conflict Resolution

> <- Back to [[Multi-Leader Replication]]

Strategies for handling conflicting writes from different leaders: last-writer-wins (LWW) using timestamps (simple but loses data), custom merge functions (application-specific logic), CRDTs (automatic conflict-free merging), and prompting the user to resolve (Google Docs approach).

#distributed-systems #replication
