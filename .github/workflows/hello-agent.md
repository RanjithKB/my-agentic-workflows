---
name: Hello Agent
on:
  workflow_dispatch:
permissions:
  contents: read
  issues: read
tools:
  github:
    toolsets: [issues]
safe-outputs:
  create-issue:
    max: 1
  add-comment:
    max: 1
    target: "*"
---

## Task

Search the open issues in this repository.
Find the issue with the most 👍 reactions.
Post a comment on that issue saying:
"This issue has the most community support! We'll prioritise it in our next planning session."

If there are no open issues, create one titled "Community Voting Test" with that same sentence as its body.
