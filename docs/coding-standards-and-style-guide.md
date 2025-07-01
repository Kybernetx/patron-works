# Coding Standards & Style Guide (Early Version)

Establishing conventions for code and content helps maintain consistency and readability—crucial for current and future development.

---

## 1. Markdown Content Style

- **Headings**: Use `#` for h1 (post title), `##` for h2, `###` for h3, etc.
- **Paragraphs**: Separate paragraphs with a blank line.
- **Emphasis**: Use `**bold**` for bold, `*italic*` for italic.
- **Lists**: Use hyphens (`-`) for unordered lists and numbers (`1.`) for ordered lists with consistent indentation.
- **Code Blocks**: Enclose code blocks with triple backticks (```) and specify the language (e.g., `python`, `js`).
- **Images**: Use `![Alt text](/path/to/image.jpg "Optional Title")`. Always include descriptive alt text.
- **Links**: Use inline links like `[Link Text](URL)`.

---

## 2. YAML Front Matter Style

- **Order**: Maintain a consistent order of fields (e.g., `title`, `date`, `description`, `tags`, `layout`).
- **Indentation**: Use 2 spaces for indentation.
- **Lists**: Use hyphenated lists for tags and categories.

---

## 3. Templating Code Style (HTML, Liquid, Go Templates, Nunjucks)

- **Indentation**: Consistent indentation (e.g., 2 spaces).
- **Commenting**: Use comments to explain complex logic or non-obvious sections.
- **Variable Naming**: Follow consistent conventions (e.g., `snake_case` for Liquid, `camelCase` for JavaScript).

---

## 4. Git Commit Messages

- **Format**: `type: Subject Line` (e.g., `feat: Add new post about AI ethics`)
- **Types**:
  - `feat`: New feature
  - `fix`: Bug fix
  - `docs`: Documentation change
  - `style`: Formatting only
  - `refactor`: Code restructuring
  - `chore`: Maintenance tasks
- **Subject**: Use concise, imperative mood (e.g., "Add," "Fix," "Update")
- **Body (Optional)**: Add a more detailed explanation if necessary.
