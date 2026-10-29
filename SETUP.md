# Set up MindRepo

MindRepo is a Markdown-based knowledgebase for AI assistants, stored in a GitHub repository you control.

## 1. Create your own private repository

Use **Use this template** on the MindRepo repository (once enabled), select **Create a new repository**, and choose **Private**. Alternatively, create a private repository and copy the template files into it.

Do **not** store personal information in a public repository. Git history may preserve information even after a file is deleted.

## 2. Connect your assistant to GitHub

Connect a GitHub integration that can read and, if desired, write repository files. Verify the integration has access to **your private copy**, not just the public template.

Capabilities depend on your assistant, account, integration permissions, and available tools. MindRepo is not an application or an automatic synchronization service.

## 3. Start the guided setup

Copy the prompt from [templates/setup-prompt.md](templates/setup-prompt.md) into a new chat. Replace the repository placeholder with your own GitHub repository name.

The assistant should inspect the repository, ask about your first topic, and propose changes **before** writing.

## 4. Add instructions to your AI project

Use [templates/project-instructions.md](templates/project-instructions.md) as a starting point for instructions in the relevant ChatGPT project or another assistant's workspace.

## 5. Verify the result

Ask the assistant to read a topic file, then explicitly request a small update. Check the resulting commit in GitHub. If the assistant cannot access GitHub, it must tell you instead of claiming that data was saved.

## Safety and workflow

- Keep your personal knowledgebase **private**.
- Do not put passwords, API keys, or credentials in Markdown.
- Review sensitive information before storing it.
- Use **direct commits to the default branch**; do not create branches or pull requests for routine knowledgebase edits.
- Always read a file before updating it. Preserve existing entries, and never force-push.
- An AI assistant cannot guarantee that it will read the repository in every chat or save information automatically.
