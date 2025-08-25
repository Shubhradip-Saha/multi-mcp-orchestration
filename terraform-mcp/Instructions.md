# Terraform MCP Server

## Requirements
- Docker installed and running
- Internet connection

## How to Use
1. Open a terminal in this folder.
2. Run the MCP server using the configuration in `mcp.json`:
   - The server will start using Docker and the official HashiCorp Terraform MCP image.
3. Example command (based on `mcp.json`):
   ```sh
   docker run -i --rm hashicorp/terraform-mcp-server
   ```
4. Follow the prompts and instructions in your terminal to interact with the MCP server.

## Notes
- Make sure Docker is running before starting the server.
- For troubleshooting, refer to HashiCorp Terraform documentation or contact your administrator.
