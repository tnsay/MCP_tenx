**TenX MCP Setup Guide**
This repository is configured to work with the TenX Feedback Analytics MCP Server via GitHub Copilot in VS Code. Follow these steps to enable the AI agent to analyze and interact with your code.

📋 Prerequisites
VS Code: Ensure your editor is updated to the latest version.

Extensions: Install both GitHub Copilot and GitHub Copilot Chat from the marketplace.

🛠️ Configuration Steps
1. Copilot Instructions
Create a custom instruction file to guide the Copilot agent:

Path: .github/copilot-instructions.md

Content: (Add your specific assignment instructions or project context here).

2. MCP Server Setup
Configure the connection between VS Code and the TenX proxy:

Create a folder named .vscode in your root directory.

Create a file inside it named mcp.json.

Click the "Add Server..." button at the bottom of the VS Code interface.

Select the server type and enter the following details:

Server URL: https://mcppulse.10academy.org/proxy

MCP Name: tenxfeedbackanalytics

3. Headers Configuration
Ensure your mcp.json includes the required headers for authentication and data routing. Your final file should look similar to this:

JSON

{
  "mcpServers": {
    "tenxfeedbackanalytics": {
      "command": "proxy",
      "args": ["https://mcppulse.10academy.org/proxy"],
      "headers": {
        "Authorization": "Bearer YOUR_TOKEN_HERE"
      }
    }
  }
}
🔌 Activation
Authenticating
Locate the tenxfeedbackanalytics server in your VS Code MCP panel.

Click the Start button.

A browser window will open; click Authorize to link your GitHub account.

Once redirected back to VS Code, your status should show as Authenticated.

Using the Tools
Open GitHub Copilot Chat (Ctrl+Shift+I).

Switch the mode to "Agent".

Click the Tools Icon to verify that the tenxfeedbackanalytics tools are visible and active.
