---
name: GitHub authentication boundaries
description: Distinguish connector authorization from Git push authentication.
---
Diagnose GitHub API access and shell Git authentication separately; do not repeatedly propose the connector to fix a shell push.

**Why:** Connector authorization attempts did not resolve Git HTTPS authentication failures, and repository creation was independently blocked by integration permissions.

**How to apply:** Check the exact failing operation and current connection status. For shell push authentication failures, direct the user to Git Providers settings or the Git pane rather than assuming a connector authorization will repair Git credentials. Never request tokens in chat.