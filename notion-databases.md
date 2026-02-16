# Notion Database Schema - The AI Agent's Compass

## 1. Prompts Database

### Properties

| Property | Type | Values | Description |
|----------|------|--------|-------------|
| Name | Title | - | Prompt Name (z.B. "System Prompt for Coding Agent") |
| Category | Select | System Prompt, Few-Shot, Negative Example, Iterative | Art des Prompts |
| Use Case | Multi-select | Coding, Writing, Research, Creative, General | Wofür der Prompt genutzt wird |
| Language | Select | English, German, Both | Sprache des Prompts |
| Model | Multi-select | GPT-4, Claude, GLM, Other | Für welche Modelle getestet |
| Status | Select | Draft, Tested, Verified, Deprecated | Status des Prompts |
| Rating | Number | 1-5 | Qualitätsscore |
| Author | Text | - | Wer hat den Prompt erstellt (Name oder "Aza") |
| Last Updated | Date | Auto | Letzte Änderung |
| Prompt | Long text | - | Der eigentliche Prompt-Text |
| Examples | Long text | - | Beispiele für die Nutzung |
| Notes | Long text | - | Zusätzliche Hinweise |

### Example Entries

1. **System Prompt - Coding Agent**
   - Category: System Prompt
   - Use Case: Coding
   - Language: English
   - Model: GPT-4, Claude
   - Status: Verified
   - Rating: 5

2. **Few-Shot - Email Writing**
   - Category: Few-Shot
   - Use Case: Writing
   - Language: German
   - Model: GPT-4
   - Status: Tested
   - Rating: 4

---

## 2. Best Practices Database

### Properties

| Property | Type | Values | Description |
|----------|------|--------|-------------|
| Name | Title | - | Name der Best Practice (z.B. "Use Chain-of-Thought for Complex Problems") |
| Use Case | Select | Coding, Writing, Research, Creative, General | Wofür die Best Practice |
| Category | Multi-select | Prompting, Tooling, Workflow, Automation, Error Handling | Art der Best Practice |
| Complexity | Select | Beginner, Intermediate, Advanced | Schwierigkeitsgrad |
| Status | Select | Draft, Verified, Deprecated | Status |
| Rating | Number | 1-5 | Qualitätsscore |
| Author | Text | - | Wer hat die Best Practice erstellt |
| Last Updated | Date | Auto | Letzte Änderung |
| Best Practice | Long text | - | Beschreibung der Best Practice |
| Examples | Long text | - | Beispiele für die Anwendung |
| Related Prompts | Relation | → Prompts Database | Verknüpfung zu Prompts |

### Example Entries

1. **Chain-of-Thought for Complex Problems**
   - Use Case: Coding, Research
   - Category: Prompting
   - Complexity: Intermediate
   - Status: Verified
   - Rating: 5

2. **Break Down Large Tasks into Sub-Tasks**
   - Use Case: General
   - Category: Workflow
   - Complexity: Beginner
   - Status: Verified
   - Rating: 4

---

## 3. Tool Integrations Database

### Properties

| Property | Type | Values | Description |
|----------|------|--------|-------------|
| Name | Title | - | Name der Integration (z.B. "OpenClaw + Notion") |
| Primary Tool | Select | OpenClaw, GitHub, Notion, Google, Moltbook, Other | Haupt-Tool |
| Secondary Tool | Select | OpenClaw, GitHub, Notion, Google, Moltbook, Other | Zweites Tool |
| Use Case | Multi-select | Automation, Workflow, Sync, Notification, API | Wofür die Integration |
| Status | Select | Draft, Tested, Production | Status |
| Complexity | Select | Beginner, Intermediate, Advanced | Schwierigkeitsgrad |
| Author | Text | - | Wer hat die Integration erstellt |
| Last Updated | Date | Auto | Letzte Änderung |
| Integration Guide | Long text | - | Schritt-für-Schritt Anleitung |
| Code Snippets | Long text | - | Beispiel-Code |
| Notes | Long text | - | Zusätzliche Hinweise |

### Example Entries

1. **OpenClaw + Notion Project Management**
   - Primary Tool: OpenClaw
   - Secondary Tool: Notion
   - Use Case: Automation, Sync
   - Status: Production
   - Complexity: Intermediate
   - Rating: 5

2. **GitHub + Discord Notifications**
   - Primary Tool: GitHub
   - Secondary Tool: Discord
   - Use Case: Notification
   - Status: Tested
   - Complexity: Beginner
   - Rating: 4

---

## 4. Errors & Solutions Database

### Properties

| Property | Type | Values | Description |
|----------|------|--------|-------------|
| Error | Title | - | Fehler-Name (z.B. "PowerShell Halluziniert `)` Syntax") |
| Error Type | Select | Syntax Error, API Error, Logic Error, Tool Error, Other | Art des Fehlers |
| Tool | Select | OpenClaw, PowerShell, Notion API, GitHub, Google, Other | In welchem Tool |
| Model | Multi-select | GPT-4, Claude, GLM, Other | Welches Model hat den Fehler generiert |
| Context | Long text | - | Was wurde gemacht |
| Error Message | Long text | - | Die genaue Fehlermeldung |
| Root Cause | Long text | - | Ursache des Fehlers |
| Solution | Long text | - | Vollständige Lösung |
| Quick Fix | Long text | - | Schnelle Workaround |
| Status | Select | Open, Solved, Workaround, Wont Fix | Status |
| Severity | Select | Critical, High, Medium, Low, Info | Schweregrad |
| Author | Text | - | Wer hat den Fehler dokumentiert |
| Last Updated | Date | Auto | Letzte Änderung |
| Related Best Practices | Relation | → Best Practices Database | Verknüpfung zu Best Practices |

### Example Entries

1. **GLM Halluziniert `)` Syntax in PowerShell**
   - Error Type: Syntax Error
   - Tool: PowerShell
   - Model: GLM
   - Status: Solved
   - Severity: High
   - Solution: Use `scripts/notion.ps1` Toolkit instead of writing PowerShell code

2. **Notion API Returns 404 for Page**
   - Error Type: API Error
   - Tool: Notion API
   - Model: Any
   - Status: Solved
   - Severity: Medium
   - Solution: Page must be shared with the integration via "Add connections"
