---
type: au.engine.readme::au-engine
tldr: Write and independently review agent skills. Load two skills and use them to develop guidance in your own package.
---

# Repo Overview

> Work in progress and not thoroughly tested.
> Expect breaking changes.

## What this is

`au-skills` helps you create and review agent skills.

## How to use this

Mount `au-skills`.
Load its two skills in your agent launch.

- **write-a-skill** creates or improves a skill, from defining its task to checking its triggers and results
- **review-a-skill** gives an existing skill or guide an independent review and reports problems with proposed fixes

Give the authoring skill a task.
Give the review skill the file to check.

## How to extend this

Keep new skills in the package that owns their task.
Supply your own examples and writing guidance.
