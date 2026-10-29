# Set up MindRepo

MindRepo is a Markdown-based knowledgebase for AI assistants, stored in a GitHub repository you control.

## 1. Create your own private repository

Use **Use this template** on the MindRepo repository, select **Create a new repository**, and choose **Private**. Alternatively, create a private repository and copy the template files into it.

Do **not** store personal information in a public repository. Git history may preserve information even after a file is deleted.

## 2. Connect your assistant to GitHub

Connect a GitHub integration that can read and, if desired, write repository files. Verify the integration has access to **your private copy**, not just the public template.

Capabilities depend on your assistant, account, integration permissions, and available tools. MindRepo is not an application or an automatic synchronization service.

## 3. Install with one prompt

Copy the complete [installation prompt](templates/setup-prompt.md) into a new chat **without changing anything**. The assistant first asks which language you prefer, then asks for your private repository name. It generates topic files and finished project instructions in your chosen language; no separate translation service is needed. **The prompt already contains the architecture, rules, and setup procedure** — you don't have to write them yourself.

The assistant checks access, asks which topics you want to remember, and designs the necessary files from your descriptions. It proposes the structure for approval **before** writing.

## 4. Paste the finished project instructions

After the approved installation, the assistant fills in the [ready-made project instructions](templates/project-instructions.md) with your repository name and gives you the **complete text to copy** into your ChatGPT project or AI workspace. You do not need to design the instructions yourself.

## 5. Verify the result

Ask the assistant to read a topic file, then explicitly request a small update. Check the resulting commit in GitHub. If the assistant cannot access GitHub, it must tell you instead of claiming that data was saved.

## Safety and workflow

- Keep your personal knowledgebase **private**.
- Do not put passwords, API keys, or credentials in Markdown.
- Review sensitive information before storing it.
- Use **direct commits to the default branch**; do not create branches or pull requests for routine knowledgebase edits.
- Always read a file before updating it. Preserve existing entries, and never force-push.
- An AI assistant cannot guarantee that it will read the repository in every chat or save information automatically.
