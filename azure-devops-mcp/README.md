# Azure DevOps MCP Server

## Requirements
- Node.js (v16 or higher recommended)
- Access to your Azure DevOps organization
- Internet connection

## How to Use
1. Open a terminal in this folder.
2. Run the MCP server using the configuration in `mcp.json`:
   - You will be prompted for your Azure DevOps organization name (e.g., `contoso`).
   - The server will start using the provided organization name.
3. Example command:
   ```sh
   npx -y @azure-devops/mcp <your-ado-org>
   ```
4. Follow the prompts and instructions in your terminal to interact with the MCP server.

## Notes
- Make sure you have the necessary permissions in your Azure DevOps organization.
- For troubleshooting, refer to Azure DevOps documentation or contact your administrator.
