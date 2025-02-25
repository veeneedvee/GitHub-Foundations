# 🚀 [Your Name] - Technical Writer Portfolio

## 🔹 About Me
I am a Technical Writer with experience in API documentation, user guides, knowledge base articles, and developer documentation. Skilled in Markdown, OpenAPI, Swagger, Postman, Git, and Docusaurus.

## 🔹 Writing Samples
### API Documentation
- 📌 [REST API Documentation Sample](#)
- 📌 [GraphQL API Documentation](#)
- 📌 [Postman API Collection](#)

### User Guides & Manuals
- 📌 [Software Installation Guide](#)
- 📌 [Cloud Security Documentation](#)
- 📌 [Product Release Notes](#)

### Knowledge Base Articles
- 📌 [Troubleshooting Common Errors](#)
- 📌 [Best Practices for API Authentication](#)

## 🔹 Tools & Technologies
✅ Postman | ✅ OpenAPI | ✅ DITA | ✅ GitHub | ✅ Markdown | ✅ Swagger | ✅ JIRA | ✅ Confluence

## 🔹 Contact
📧 Email: [Your Email]  
🔗 LinkedIn: [Your LinkedIn]  
🌐 Website: [Your Portfolio Website]


Here are portfolio templates for Docusaurus, Swagger UI, and MkDocs to help you showcase your technical writing skills.

## 🚀 1. Docusaurus-Based Portfolio Template

Docusaurus is a powerful open-source documentation site generator.

### 📌 Steps to Set Up Your Portfolio
1. Install Docusaurus

```
npx create-docusaurus@latest my-portfolio classic
cd my-portfolio
npm run start
```

2. Customize the Homepage

Edit `src/pages/index.js` with your portfolio content.

3. Create Documentation Pages

   * Add API docs, user guides, knowledge base articles under `docs/`.
   * Example: `docs/api-documentation.md`

4. Deploy on GitHub Pages

```
GIT_USER=<YourGitHubUsername> USE_SSH=true npm run deploy
```

### 📌 Sample Portfolio Content (src/pages/index.js)

```
import React from 'react';

export default function Home() {
  return (
    <main>
      <h1>👋 Hi, I'm [Your Name]</h1>
      <p>Technical Writer | API Documentation | DevOps Docs</p>

      <h2>📄 Portfolio</h2>
      <ul>
        <li><a href="/docs/api-documentation">API Documentation</a></li>
        <li><a href="/docs/user-guide">User Guide</a></li>
        <li><a href="/docs/troubleshooting-guide">Troubleshooting Guide</a></li>
      </ul>

      <h2>📬 Contact</h2>
      <p>Email: [your-email@example.com]</p>
      <p>LinkedIn: <a href="https://linkedin.com/in/yourprofile">Your Profile</a></p>
    </main>
  );
}
```

🔗 Live Example → https://docusaurus.io/showcase

## 📖 2. Swagger UI-Based API Documentation Portfolio

Swagger UI helps create interactive API documentation.

### 📌 Steps to Set Up Swagger UI

1. Create an OpenAPI YAML File (api-docs.yaml)

```
openapi: 3.0.0
info:
  title: My API Portfolio
  description: API Documentation Portfolio of [Your Name]
  version: 1.0.0
paths:
  /login:
    post:
      summary: User Login API
      requestBody:
        required: true
        content:
          application/json:
            schema:
              type: object
              properties:
                username:
                  type: string
                password:
                  type: string
      responses:
        200:
          description: Successful login
```

2. Host it using Swagger UI

   * Upload it to Swagger Editor → https://editor.swagger.io/
   * Deploy it using Swagger Hub

🔗 Live Example → https://editor.swagger.io/

## 📚 3. MkDocs-Based Portfolio Template

MkDocs is a lightweight static site generator for documentation.

### 📌 Steps to Set Up Your Portfolio

1. Install MkDocs

```
pip install mkdocs
```

2. Create a New MkDocs Project

```
mkdocs new my-portfolio
cd my-portfolio
```

3. Modify `mkdocs.yml` (Configuration File)

```
site_name: "[Your Name] - Technical Writing Portfolio"
nav:
  - Home: index.md
  - API Docs: api-docs.md
  - User Guides: user-guide.md
  - Troubleshooting: troubleshooting.md
theme:
  name: material
```

4. Add Portfolio Content (`docs/index.md`)

```
# 👋 Hi, I'm [Your Name]
## 📝 Technical Writer | API Docs | DevOps Docs
- [API Documentation](api-docs.md)
- [User Guide](user-guide.md)
- [Troubleshooting Guide](troubleshooting.md)
```

5. Run the Local Server

```
mkdocs serve
```

6. Deploy on GitHub Pages

```
mkdocs gh-deploy
```

🔗 Live Example → https://squidfunk.github.io/mkdocs-material/
