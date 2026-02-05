## 🧠 PROMPT — Simple, Comprehension-First Notes (with Inline Code)

Turn the provided **TEXT** into **study notes** for learning and review.

Stay close to the **original wording** when it improves clarity/precision. Light paraphrase is allowed, but **do not remove useful context or detail**. Remove **only** fluff, repetition, and persuasion.

---

### 🎯 Goals

- Preserve the **original idea order**
- Preserve the **exact order code appears in the source**
- Keep **all** important facts, rules, explanations, context, and **all code**
- Prioritize **comprehension over brevity** (expand if it helps learning)
- Prefer **simple, plain language**

---

### 🧱 Structure (Notion-Ready)

- Use **nested collapsible toggles** for organization
- Toggle headings use: `▶#`, `▶##`, `▶###`
- Regular toggles use: `▶ <text>`
- Nest children with **tabs** (not spaces)
- The **deepest content nodes** must be **list items**:
    - Use **bullet list items ()** for facts/notes/examples/options (non-sequential)
    - Use **ordered list items (`1.` `2.` `3.`)** for steps/procedures/sequences (ordered)
- Nesting list items is allowed when it improves clarity
- **Code blocks go inside the toggle/list structure**, indented to match the parent level
- No artificial limits on list length

---

### 😀 Emoji Rules

- Choose **one meaningful emoji** for each toggle line or list item (definition/rule/process/example/warning/tool/etc.)
- Place the emoji at the **very beginning** of every **toggle** or **list item** line
- Emojis must match the line’s content

---

### ✏️ Line Rules

Each non-code line must:

- Start with **exactly one emoji + one space**
- Express **one idea only**

---

### 🏷️ Headers & Subheaders (Numbering + Unlimited Depth)

**⚠️ CRITICAL: Every header MUST be a toggle heading (`▶#` / `▶##` / `▶###`). NEVER use plain headings (`#` / `##` / `###`). If a header does not start with `▶`, it is wrong — go back and fix it.**

- First-level headers must be written as:
    - `▶# <emoji> 1. <Header Title>`
- Subheaders must use hierarchical numbering:
    - `▶## <emoji> 1.1. <Subheader Title>`
    - `▶### <emoji> 1.1.1. <Sub-subheader Title>`

**Deeper than Level 3**

- Continue hierarchical numbering as deep as needed while using `▶###`:
    - `▶### <emoji> 1.1.1.1. <Title>`
    - `▶### <emoji> 1.1.1.1.1. <Title>`
- Titles must **name the concept**
- **Uncollapse all toggle headings immediately after creating them** so content is visible by default

**⚠️ POST-CREATION CHECK (MANDATORY):**

- After finishing all content, **scan every heading** in the output.
- If **any** heading uses `#`, `##`, or `###` without the `▶` prefix, **replace it** with the corresponding toggle heading (`▶#`, `▶##`, `▶###`).
- This check must happen **every time**, no exceptions.

---

### 📛 Proper Nouns

- Format all proper nouns as: `**Proper Noun***`
- If unsure, **format it anyway**

---

### 💻 Code Handling (STRICT + INLINE + ORDERED)

- **Preserve every code snippet/command/config exactly**
- Do **not** rewrite, rename, simplify, or reorder code
- Do **not** execute, run, or interpret code
- Code must appear in the **same chronological order** as the source

**Code Placement Rules**

- Code blocks must:
    - Appear **immediately after** the toggle/list item that introduces them
    - Be **indented with tabs** to match the nesting level of their parent
    - Use **fenced code blocks** with a language tag when obvious
    - Stay **inside** the toggle/list structure (never unindented/outside)

If code is referenced but not shown in the source, add a separate line:

- `🕳️ Missing or unclear detail: "<exact phrase>"`

---

### 🕳️ Missing or Unclear Information

If something is referenced but not explained:

- Keep the reference
- Add a separate line:
    - `🕳️ Missing or unclear detail: "<exact phrase>"`

---

### 📥 Input

Use the provided source material **exactly as given**.

---

### 🚨 FINAL STEP — TOGGLE HEADING ENFORCEMENT (DO THIS LAST)

**After ALL content has been generated, you MUST perform this final pass before finishing:**

1. Go through **every single heading** in your entire output, line by line.
2. Check: Does it start with `▶`? 
    - ✅ `▶# ...` → correct, leave it
    - ✅ `▶## ...` → correct, leave it
    - ✅ `▶### ...` → correct, leave it
    - ❌ `# ...` (missing `▶`) → **REPLACE** with `▶# ...`
    - ❌ `## ...` (missing `▶`) → **REPLACE** with `▶## ...`
    - ❌ `### ...` (missing `▶`) → **REPLACE** with `▶### ...`
3. **There must be ZERO plain headings in the final output.** Every heading must be a toggle heading.
4. **Do not skip this step.** Do not assume earlier output was correct. Actually re-check.
5. If you find even one plain heading, fix it before delivering the output.

**This is non-negotiable. The output is not complete until this check has been performed and all headings are toggle headings.**
