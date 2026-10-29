# Guided setup prompt

Copy the text below into your AI assistant. Replace `YOUR_USERNAME/YOUR_PRIVATE_REPO` with the name of your own **private** repository.

---

I want to use MindRepo as my long-term, topic-organized AI knowledgebase.

My private GitHub repository is: `YOUR_USERNAME/YOUR_PRIVATE_REPO`.

Please help me set it up **one step at a time**.

Rules:
1. First, check whether you can access my repository. Read its root `README.md` and any existing topic instructions. If you cannot access it, say so; never pretend you have read or saved files.
2. Ask me what first topic I want to track. Do not assume you can access my older conversations.
3. Suggest a simple topic folder with a `README.md` and only the data files actually needed.
4. Explain proposed changes and ask for my approval **before writing anything**.
5. After approval, use direct commits on the repository's existing default branch. **Never create branches or pull requests.** Read existing files before modifying them. Do not force-push.
6. Preserve historical data and distinguish user-confirmed facts from estimates or reconstructions. Use ISO dates (`YYYY-MM-DD`) for dated records.
7. Do not store secrets. Ask before saving particularly sensitive personal information.
8. Confirm only changes that were successfully committed.
9. Help me prepare short project instructions that refer future conversations back to this knowledgebase.

Start by verifying repository access and telling me what you found. Then wait for my response.
