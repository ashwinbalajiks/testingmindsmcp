# TestingMinds MCP Tutorial

Practical QA workflows using **Chrome DevTools MCP** and **GitHub Copilot Agent Mode**.

This repository demonstrates how AI agents can perform:

- 🚀 Quick Deployment Readiness Assessment
- 🔍 Full Deployment Readiness Assessment
- 📊 Professional HTML Report Generation
- 🤖 Test Automation Generation

---

# Repository

```text
https://github.com/ashwinbalajiks/testingmindsmcp.git
```

---

# Prerequisites

Before starting, ensure you have the following installed:

- Visual Studio Code (latest)
- Git
- Node.js 20+
- Google Chrome
- GitHub Copilot (Free or Pro)

> **Note:** GitHub Copilot Free works with this repository. Premium models will generally complete assessments faster.

---

# 1. Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/ashwinbalajiks/testingmindsmcp.git

cd testingmindsmcp
```

---

# 2. Open the Project

Open the project in Visual Studio Code.

```bash
code .
```

or

**File → Open Folder**

---

# 3. Configure Chrome DevTools MCP

This repository contains a **`.vscode`** folder.

Inside the project, create (or update) the following file:

```text
.vscode/mcp.json
```

Add the following MCP server configuration:

```json
{
    "servers": {
        "io.github.ChromeDevTools/chrome-devtools-mcp": {
            "command": "npx",
            "args": [
                "-y",
                "chrome-devtools-mcp@latest"
            ]
        }
    }
}
```

Save the file.

Reload Visual Studio Code.

---

# 4. Available Agents

| Agent | Description |
|---------|-------------|
| **QQRA** | Quick Deployment Readiness Assessment |
| **QDRA** | Full Deployment Readiness Assessment |
| **QRG** | Professional HTML Report Generator |
| **QTAG** | Test Automation Generator |

---

# 5. Demo Application

Use the following application during the workshop:

```
https://qa-readiness-ik9w1gvr5-ashwinbalajiks-projects.vercel.app
```

---

# 6. Quick Readiness Assessment (Recommended)

Select the **QQRA** agent.

Run the following prompt:

```text
Test the deployment readiness of

https://qa-readiness-ik9w1gvr5-ashwinbalajiks-projects.vercel.app
```

QQRA performs a lightweight readiness assessment and generates a concise HTML report.

---

# 7. Full Deployment Readiness Assessment

Select the **QDRA** agent.

Run:

```text
Test the deployment readiness of

https://qa-readiness-ik9w1gvr5-ashwinbalajiks-projects.vercel.app
```

QDRA performs a comprehensive readiness assessment and generates structured assessment artifacts.

---

# 8. Professional Report Generation

After QDRA completes, select the **QRG** agent.

Run:

```text
Generate the professional readiness report from the latest QDRA run.
```

QRG generates an executive-ready HTML report containing:

- Executive Summary
- Coverage Metrics
- Page Analysis
- Network Analysis
- Console Analysis
- Findings
- Embedded Evidence
- Recommendations

---

# 9. Test Automation Generation

Select the **QTAG** agent.

Run:

```text
Generate Robot Framework Browser Library automation from the latest QDRA run.
```

QTAG generates reusable automation based on the assessed workflows.

---

# Project Structure

```text
testingmindsmcp
│
├── .github
│   ├── agents
│   │   ├── QQRA.agent.md
│   │   ├── QDRA.agent.md
│   │   ├── QRG.agent.md
│   │   └── QTAG.agent.md
│   │
│   └── copilot-instructions.md
│
├── .vscode
│   └── mcp.json
│
├── prompts
│
├── templates
│
├── README.md
│
└── .gitignore
```

---

# Notes

- QQRA is designed for fast deployment readiness checks.
- QDRA performs a deeper assessment.
- QRG converts assessment evidence into a professional HTML report.
- QTAG generates automation from the assessment output.

---

# License

MIT License
