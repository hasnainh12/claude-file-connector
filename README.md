Claude Desktop File Connector

A custom MCP (Model Context Protocol) server that allows Claude Desktop to securely access files and folders on your local computer.

Features:
1. Token Optimization: Uses project_map, outline_file, and read_symbol tools to read only the relevant sections instead of entire files, saving context and tokens.
2. Safety First (Read-Only by Default): No files are written or edited by default. You must explicitly set "allowWrites": true in config.json to enable write access.
3. Native Popup Approval: When Claude attempts to write or edit a file, a native Windows popup (Yes/No) appears for manual approval.
4. Security: Blocks access to secret files (like .env, id_rsa). Prevents path traversal attacks using UNC, ADS, and symlinks.
5. Deduplication: Prevents reading the same file twice in a session if it hasn't been modified.

Setup Instructions:

Step 1: Download the Connector
Go to the top of this repository page and click the green "<> Code" button. Select "Download ZIP". Once downloaded, extract the ZIP file to a folder on your computer (e.g., C:\claude-file-connector).

Step 2: Install Node.js (If not installed)
Ensure you have Node.js installed. You can download it from nodejs.org.

Step 3: Install Dependencies
Open Command Prompt or PowerShell. Navigate to the folder where you extracted the connector (e.g., cd C:\claude-file-connector). Run the command: npm install

Step 4: Configure Your Folders
Open the config.json file in the extracted folder using Notepad or any text editor. Update the "allowedFolders" and "writableFolders" arrays with the paths to the folders you want Claude to access. Use double backslashes (\\) for Windows paths.

Step 5: Connect to Claude Desktop
Open your Claude Desktop configuration file. You can find it at C:\Users\YourName\AppData\Roaming\Claude\claude_desktop_config.json. Add the file-connector configuration inside the "mcpServers" object.

Step 6: Restart Claude Desktop
Close Claude Desktop completely (including from the system tray). Open Claude Desktop again. You can now ask Claude to list or read files from your allowed folders!

Usage:
Once connected, simply ask Claude to check your files. For example:
- "Set active folder to Documents"
- "List files in my current folder"
- "Read the file market_analyzer.py"
