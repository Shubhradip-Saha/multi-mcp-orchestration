# Multi-MCP Orchestration

## Usage
- This setup allows you to run both Terraform MCP and Azure DevOps MCP servers together.
- Open two terminals in this folder:
  - In one, run the Terraform MCP server:
    ```sh
    docker run -i --rm hashicorp/terraform-mcp-server
    ```
  - In the other, run the Azure DevOps MCP server:
    ```sh
    npx -y @azure-devops/mcp <your-ado-org>
    ```
- Running both servers simultaneously enables the agent to update and orchestrate context across both platforms.
