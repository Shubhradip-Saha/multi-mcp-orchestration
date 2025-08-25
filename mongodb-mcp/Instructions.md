# MongoDB MCP Server

## Requirements
- Docker installed and running
- MongoDB Atlas API credentials (for AtlasAPI)
- MongoDB connection string (for Connection-String)
- Internet connection

## How to Use

### AtlasAPI
1. Open a terminal in `mongodb-mcp/AtlasAPI`.
2. Update `mcp.json` with your Atlas Service Account credentials.
3. Run the MCP server using Docker:
   ```sh
   docker run --rm -i \
     -e MDB_MCP_READ_ONLY=true \
     -e MDB_MCP_API_CLIENT_ID=your-atlas-service-accounts-client-id \
     -e MDB_MCP_API_CLIENT_SECRET=your-atlas-service-accounts-client-secret \
     mongodb/mongodb-mcp-server:latest
   ```

### Connection-String
1. Open a terminal in `mongodb-mcp/Connection-String`.
2. Update `mcp.json` with your MongoDB connection string and credentials.
3. Run the MCP server using Docker:
   ```sh
   docker run --rm -i \
     -e MDB_MCP_CONNECTION_STRING="mongodb+srv://username:password@cluster.mongodb.net/myDatabase" \
     -e MDB_MCP_READ_ONLY=true \
     mongodb/mongodb-mcp-server:latest
   ```

## Notes
- Replace all placeholder values with your actual credentials.
- Make sure Docker is running before starting the server.
- For troubleshooting, refer to MongoDB documentation or contact your administrator.
