# MCP Servers Workspace

Hello everyone!

This repository contains some sample multiple MCP (Model Context Protocol) server configurations and orchestration setups for Azure DevOps, Contentstack, Terraform, MongoDB, and GitHub. Each folder provides instructions and configuration files for running and integrating MCP servers with various platforms.
It will help you get started with MCP server implementation into your project. 

**However always use this for Testing or Dev, avoid Production**

## Points to Note

1) Running MCP server locally / project based.

- To run an MCP server in VS Code, create a `.vscode` folder in your workspace and paste the required `mcp.json` configuration file inside it. After saving the `mcp.json` file in VS Code, you will see an inline Start button. Click it to launch the MCP server.
- For Cursor editor, create a `.cursor` folder and place the respective configuration file (e.g., `mcp.json`) inside it.
- Make sure to use the correct configuration for the platform you want to orchestrate.
- Always replace placeholder values in configuration files with your actual credentials and settings.

2) Running MCP server in global settings.

- You can change the `user-preference.json` file in your editor's global settings and add the MCP server configuration you want.
- For global configuration, you must add the `mcpServers {}` parent block in your JSON file.
- Only the 'mcp.json' scripts containing the `mcpServers {}` block are meant to be run globally.
- This allows you to orchestrate MCP servers across all projects, not just the current workspace.
- In Cursor go to cursor settings and search for MCP and Integration and select the mcp server you want to use, selecting multiple results in limiting the total tool uses as one needs to accommodate within 128.
- One can run multiple mcp servers together. All will update the context of agent simultaneously.

3) Requirements:

- Docker Desktop is required for MCP servers that use Docker (e.g., Terraform, MongoDB, GitHub MCP servers).
- NPX (Node.js) is required for MCP servers that use NPX commands (e.g., Azure DevOps, Contentstack MCP servers).
- Ensure you have the necessary credentials and API tokens for each platform.
- Agent enabled and has access to codebase.

4) All of them are MCP servers we run locally.

5) Agent should have restricted permissive access to the directory. It should only have access to the current directory or n-1.

6) Security & Best Practices:

- Always add `.vscode/`, `.cursor/`, `.env`, and `.github/` to your `.gitignore` file to prevent pushing editor config folders, secrets, and workflow files that may contain credentials or sensitive instructions.
- Use a `.env` file to store sensitive environment variables and secrets securely. Never commit your `.env` file to version control.
- Regularly review your configuration files to ensure no secrets are exposed.
- Try to restrict the .env file's access from the agent/ don't update the .env file in the agent's content for safety against rogue changes.

7) Directory Structure & Usage:

- You need three main directories:
  - `.cursor` or `.vscode`: For configuration files, `mcp.json`, and agentic instruction files.
  - `.env`: For storing tokens, credentials, and secrets.
  - `.github`: For storing workflows and MDC instruction files for the agent to follow.
  - In Cursor, you can add configuration through Cursor settings (General and Project Specific). For project-specific configuration, add the MDC file in the `.cursor` directory.
  - `.gitignore` file to avoid pushing the above directories and files to your remote repository.

