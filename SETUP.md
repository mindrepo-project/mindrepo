# Set up MindRepo

MindRepo is a Markdown-based knowledgebase for AI assistants, stored in a GitHub repository you control.

## 1. Create your own private repository

Use **Use this template** on the MindRepo repository, select **Create a new repository**, and choose **Private**. Alternatively, create a private repository and copy the template files into it.

Do **not** store personal information in a public repository. Git history may preserve information even after a file is deleted.

## 2. Connect your assistant to GitHub

Connect a GitHub integration that can read and, if desired, write repository files. Verify the integration has access to **your private copy**, not just the public template.

Capabilities depend on your assistant, account, integration permissions, and available tools. MindRepo is not an application or an automatic synchronization service.

## GitHub access troubleshooting

If the assistant cannot read your private repository or a write fails:

1. Check that the GitHub integration is connected to the correct account.
2. Confirm that the integration can access **your private repository**, not just the public MindRepo template. If repository access is restricted, explicitly allow your private repository.
3. Check the integration's repository permissions: reading files is required for recall, and writing files is required for saving.
4. For repositories owned by a GitHub organisation, check whether the organisation requires separate integration authorisation or approval.
5. Ask the assistant to **read an existing file first**, then approve a small test edit and verify the commit on GitHub.

Available integration settings differ between AI assistants and accounts. If a tool is missing or a write fails, do not assume that anything was saved. Never paste access tokens into a chat to work around permission problems.

## 3. Install with one prompt

Copy the complete [installation prompt](templates/setup-prompt.md) into a new chat **without changing anything**. The assistant uses your preferred language when it can reliably determine it from available context, or asks you to choose if uncertain. Then it asks for your private repository name. It generates topic files and finished project instructions in your chosen language; no separate translation service is needed. **The prompt already contains the architecture, rules, and setup procedure** — you don't have to write them yourself.

The assistant checks access, then asks whether you want to describe a **custom topic** or get inspiration from one or more [topic examples](README.md#-what-could-you-remember). Each example includes fictional demo records and sample prompts; these are never imported as your personal data. The examples are **ideas only, not templates to copy**. The assistant must not reuse their contents, filenames, directory structures, or recording rules. Instead it proposes an original personal structure based on your answers. It proposes the structure for approval **before** writing.

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
