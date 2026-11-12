---
name: linear-service
description: Select the intended workspace when Linear work spans multiple accounts or connections.
metadata:
  version: "0.1.0"
---

Bind each task to its intended workspace before accessing workspace content.
Keep that binding throughout the task. When the requested workspace is ambiguous,
resolve it with the user rather than choosing whichever connection succeeds.
An access denial does not authorize trying the same operation in another workspace.
