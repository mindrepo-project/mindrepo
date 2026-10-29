# MindRepo

**Your AI's memory. Your repository. Your control.**

Give your AI a persistent, structured memory using GitHub. **No database, no server, just Markdown.**

MindRepo is a lightweight, open template for keeping useful knowledge from AI conversations in a **private GitHub repository you own**. Instead of relying entirely on one chat's context, organize durable facts, decisions, notes, and ongoing records into readable topic files.

> **MindRepo is a template and workflow, not a hosted service.** It requires an AI assistant with an appropriate GitHub integration. Automatic memory retrieval, writing, and background synchronization are **not guaranteed**.

## Why MindRepo?

- **You own the data.** Plain Markdown and CSV files, stored in your private repository.
- **Organized by topic.** Each topic has its own README, files, and recording rules.
- **Readable by humans and AI.** No proprietary database format.
- **Version history.** Git commits show what changed and when.
- **Portable approach.** Adapt the same files to other assistants with repository access.
- **Minimal setup.** No app server, vector database, or custom MCP server required for the basic workflow.

## Quick start

1. Click **Use this template** → **Create a new repository** (after template mode is enabled), and set **visibility to Private**. Alternatively, copy these files into a new private repository.
2. Connect an AI assistant to GitHub with access to **your private copy**.
3. Follow the [setup guide](SETUP.md).
4. Paste the [guided setup prompt](templates/setup-prompt.md) into your assistant, replacing the repository placeholder.
5. Add [project instructions](templates/project-instructions.md) to your AI project or workspace.
6. Test reading and writing a sample entry, and verify the commit on GitHub.

**Never put personal information into a public fork or public repository.** This public repository contains fictional examples only.

## How it works

```text
Your conversation
       |
       v
AI assistant + GitHub integration
       |
       v
Your PRIVATE GitHub repository
  README.md                 <- shared conventions
  topics/
    health/README.md        <- topic-specific rules
    travel/README.md        <- another topic
    ...
```

The assistant reads relevant topic instructions when needed, and can update files **if** its integration has write access and you have authorized the workflow. GitHub holds the durable records; the chat remains the interface.

## Included files

| File | Purpose |
| --- | --- |
| [SETUP.md](SETUP.md) | Step-by-step setup and safety guidance |
| [templates/setup-prompt.md](templates/setup-prompt.md) | Copy-paste prompt for guided onboarding |
| [templates/project-instructions.md](templates/project-instructions.md) | Reusable instructions for an AI project |
| [templates/topic-readme.md](templates/topic-readme.md) | Starting point for a new topic |
| [topics/example/](topics/example/README.md) | Fictional reading-log example |

## Ground rules

1. **Private by default for personal data.** This public repository is only a template.
2. **No invented history.** Label estimates and reconstructed information.
3. **No silent overwrites.** Read files before editing; preserve existing records.
4. **No branches or PRs for routine updates.** Commit directly to the existing default branch; never force-push.
5. **No secrets.** Do not commit credentials, tokens, or API keys.
6. **No false save confirmations.** If the assistant cannot access GitHub or a write fails, it must say so.

## Limitations

- GitHub access and write permissions vary by assistant and integration.
- AI project instructions cannot guarantee that every new chat will load these files.
- This is not a background synchronization system or a replacement for backups.
- You remain responsible for deciding which personal information to store.

## Contributing

Suggestions and improvements are welcome. For personal knowledgebase edits, the recommended workflow is direct commits to your **own private repository**. This does not require publishing personal data.

## License

See [LICENSE](LICENSE) for license terms.
