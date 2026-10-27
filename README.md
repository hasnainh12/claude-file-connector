# Claude Desktop File Connector

A custom MCP (Model Context Protocol) server that allows Claude Desktop to securely access files and folders on your local computer.

## ✨ Features
- **Token Optimization:** Uses `project_map`, `outline_file`, and `read_symbol` tools to read only the relevant sections instead of entire files, saving context and tokens.
- **Safety First (Read-Only by Default):** No files are written or edited by default. You must explicitly set `"allowWrites": true` in `config.json` to enable write access.
- **Native Popup Approval:** When Claude attempts to write or edit a file, a native Windows popup (Yes/No) appears for manual approval.
- **Security:** Blocks access to secret files (like `.env`, `id_rsa`). Prevents path traversal attacks using UNC, ADS, and symlinks.
- **Deduplication:** Prevents reading the same file twice in a session if it hasn't been modified.

## 🚀 Setup Instructions

### Step 1: Download the Connector
- Go to the top of this repository page and click the green **"<> Code"** button.
- Select **"Download ZIP"**.
- Once downloaded, extract the ZIP file to a folder on your computer (e.g., `C:\claude-file-connector`).

### Step 2: Install Node.js (If not installed)
Ensure you have Node.js installed. You can download it from [nodejs.org](https://nodejs.org/).

### Step 3: Install Dependencies
- Open **Command Prompt** or **PowerShell**.
- Navigate to the folder where you extracted the connector:
  ```bash
  cd C:\claude-file-connector
