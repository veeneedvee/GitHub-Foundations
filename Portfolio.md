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

```sh
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

```sh
GIT_USER=<YourGitHubUsername> USE_SSH=true npm run deploy
```

### 📌 Sample Portfolio Content (src/pages/index.js)

```jsx
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

```yaml
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

```sh
pip install mkdocs
```

2. Create a New MkDocs Project

```sh
mkdocs new my-portfolio
cd my-portfolio
```

3. Modify `mkdocs.yml` (Configuration File)

```yaml
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

```md
# 👋 Hi, I'm [Your Name]
## 📝 Technical Writer | API Docs | DevOps Docs
- [API Documentation](api-docs.md)
- [User Guide](user-guide.md)
- [Troubleshooting Guide](troubleshooting.md)
```

5. Run the Local Server

```sh
mkdocs serve
```

6. Deploy on GitHub Pages

```sh
mkdocs gh-deploy
```

🔗 Live Example → https://squidfunk.github.io/mkdocs-material/

Here are Docusaurus and MkDocs portfolio templates tailored for Technical Writers. These templates will help you build a structured portfolio showcasing your documentation skills.

## 📌 Docusaurus Portfolio for Technical Writers
Docusaurus is a great choice if you want an interactive, well-structured documentation website.

### 🚀 Steps to Set Up

1. Install Docusaurus

```sh
npx create-docusaurus@latest my-portfolio classic
cd my-portfolio
npm run start
```

2. Modify Homepage (`src/pages/index.js`)

```jsx
import React from 'react';
import Layout from '@theme/Layout';

export default function Home() {
  return (
    <Layout title="Technical Writing Portfolio">
      <div style={{ textAlign: 'center', padding: '50px' }}>
        <h1>🚀 Welcome to My Portfolio</h1>
        <p>I specialize in API documentation, developer guides, and user manuals.</p>
        <a href="/docs">View My Work</a>
      </div>
    </Layout>
  );
}
```

3. Create a Portfolio Section (`docs/portfolio.md`)

```md
# 📌 Technical Writing Portfolio

## 🔹 API Documentation
- [REST API Docs](api-docs/rest-api)
- [GraphQL API Docs](api-docs/graphql)

## 🔹 User Guides
- [Software Installation Guide](guides/software-installation)
- [Feature Walkthroughs](guides/feature-walkthrough)

## 🔹 Knowledge Base Articles
- [Troubleshooting Common Issues](kb/troubleshooting)
- [Best Practices for Documentation](kb/best-practices)

## 🔹 Contact
📧 Email: your.email@example.com  
🔗 LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)  
🌐 Portfolio: [Your Website](https://yourportfolio.com)
```

4. Add Navigation to `sidebars.js`

```js
module.exports = {
  sidebar: [
    {
      type: 'category',
      label: 'Portfolio',
      items: ['portfolio'],
    },
  ],
};
```

5. Deploy to GitHub Pages

```sh
GIT_USER=<YourGitHubUsername> USE_SSH=true npm run deploy
```

👉 Live Example: Docusaurus Showcase

## 📌 MkDocs Portfolio for Technical Writers

MkDocs is a lightweight, Markdown-based documentation framework.

### 🚀 Steps to Set Up

1. Install MkDocs

```sh
pip install mkdocs
```

2. Create a New Project

```sh
mkdocs new my-portfolio
cd my-portfolio
```

3. Modify Configuration (`mkdocs.yml`)

```yaml
site_name: "Technical Writing Portfolio"
theme: material
nav:
  - Home: index.md
  - Portfolio:
      - API Documentation: api-docs.md
      - User Guides: user-guides.md
      - Knowledge Base: knowledge-base.md
  - Contact: contact.md
```

4. Edit Homepage (docs/index.md)

```md
# 🚀 Welcome to My Portfolio

## 🔹 About Me
I am a Technical Writer specializing in API documentation, developer guides, and knowledge bases.

## 🔹 My Work
- [API Documentation](api-docs.md)
- [User Guides](user-guides.md)
- [Knowledge Base](knowledge-base.md)

## 🔹 Contact
📧 Email: your.email@example.com  
🔗 [LinkedIn](https://linkedin.com/in/yourprofile) 
```

5. Create API Documentation Page (`docs/api-docs.md`)

```md
# 📌 API Documentation Samples

## 🔹 REST API
- [Authentication API](rest-authentication.md)
- [User Management API](rest-users.md)

## 🔹 GraphQL API
- [Query Example](graphql-query.md)
- [Mutation Example](graphql-mutation.md)
```

6. Run Local Server

```sh
mkdocs serve
```

Open __http://127.0.0.1:8000/__ in your browser.

7. Deploy to GitHub Pages

```sh
mkdocs gh-deploy
```

👉 Live Example: MkDocs Material Theme

💡 Which One Should You Use?
* _Docusaurus_ → Best for an interactive and professional-looking documentation website.
* _MkDocs_ → Best for a lightweight, Markdown-based portfolio that’s easy to maintain.

