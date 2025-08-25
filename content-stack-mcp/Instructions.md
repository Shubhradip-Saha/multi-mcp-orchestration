# Configure MCP for Contentstack

## Instructions

### 1. Add the `claude_desktop_config.json` in Claude

To add or update your Claude configuration:
1. Open Claude Desktop.
2. Click the Claude icon in the top-left corner of the window.
3. Select **Settings** from the dropdown menu.
4. In the Settings pop-up, go to the **Developer** tab.
5. Click **Edit Config**.
6. Claude will redirect you to the `claude_desktop_config.json` file where you can add or update the configuration.
7. Add or update your MCP configuration as needed (see `mcp.json`).

### 2. About the `mcp.json` file
- Place your `mcp.json` in this folder and update the placeholder values with your actual Contentstack and Lytics credentials.

### 3. Notes on Environment Variables
- `CONTENTSTACK_DELIVERY_TOKEN`: Only needed for delivery API tools (CDA).
- `CONTENTSTACK_BRAND_KIT_ID`: Required for Brand Kit related tools.
- `LYTICS_ACCESS_TOKEN`: Required for Lytics analytics tools.
- `CONTENTSTACK_PERSONALIZE_PROJECT_ID`: Required for Personalize tools.
- `CONTENTSTACK_LAUNCH_PROJECT_ID`: Required only for Launch tools.
- `GROUPS`: Specifies a comma-separated list of API groups to enable. Allowed values are `cma` (default), `cda`, `analytics`, `brandkit`, `launch`, `lytics`, `personalize`, and `all`.

## Requirements
- Node.js (v16 or higher recommended)
- Contentstack API credentials
- Lytics token (if using analytics tools)

## How to Use
1. Open a terminal in this folder.
2. Run the MCP server using the configuration in `mcp.json`:
   ```sh
   npx -y @contentstack/mcp
   ```
3. Follow the prompts and instructions in your terminal to interact with the MCP server.
