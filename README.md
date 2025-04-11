⚙️ How to Set Up a Local MCP Server with Cursor IDE
Follow the steps below to run your own MCP server locally and test it using custom tool commands in Cursor IDE.

🛠️ Files Included
mcp_server.py
The Python script that runs the local MCP server.

mcp_local_mcp_server_settings_for_Cursor_IDE.json
Configuration to register the MCP server in Cursor IDE.

🚀 Steps to Set Up the MCP Server
Ensure Python is Installed
Run the following in your terminal to check:

bash
Copy
Edit
python3 --version
If not installed, download it from https://www.python.org/downloads.

Run the MCP Server
In the terminal, navigate to the folder where mcp_server.py is located and run:

bash
Copy
Edit
python3 mcp_server.py
✅ This starts the server on 127.0.0.1:8080.

🧩 Add MCP Server to Cursor IDE
Open Cursor Settings
Go to Settings → Experimental → MCP Servers.

Add the Configuration
Paste the following into the MCP settings in Cursor:

json
Copy
Edit
{
  "mcpServers": {
    "MCP-text-analysis": {
      "command": "python",
      "args": ["/Users/vijender/Desktop/MCP_Project/server.py"],
      "host": "127.0.0.1",
      "port": 8080,
      "timeout": 30000
    }
  }
}
⚠️ Important:
Update the path in "args" to match the actual location of your mcp_server.py file.

🧪 How to Use the MCP Server in Cursor
Launch the MCP Server
Make sure the server is running via the terminal.

Open Cursor IDE
Press Cmd+K (Mac) or Ctrl+K (Windows/Linux) to open the command palette.

Run a Chat Command
Use natural language like:

pgsql
Copy
Edit
Use MCP-text-analysis to analyze this paragraph for key insights.
You can also select text in your file, right-click, and use MCP actions if they appear in the context menu.

View the Result
The output will be shown in the chat interface or editor depending on how Cursor is configured.

📌 Notes
Make sure no other application is using port 8080.

Always start the MCP server before using it in Cursor.

Cursor communicates with MCPs using the OpenMCP protocol.

🧯 Troubleshooting
Having issues? Try these:

🔁 Command not responding?
Ensure the mcp_server.py script is actively running without errors.

📂 Incorrect file path?
Double-check the "args" path in your JSON configuration.

🛑 Port in use?
Kill any process already using port 8080 or change the port number in both the server script and Cursor config.


# 🔥 How to Get a Firecrawl API Key

Follow the steps below to obtain your Firecrawl API key and start integrating it into your applications.

---

## 🚀 Steps to Generate an API Key

1. **Go to the API Key Page**  
   Open [https://www.firecrawl.dev/app/api-keys](https://www.firecrawl.dev/app/api-keys) in your web browser.

2. **Sign In to Firecrawl**  
   If you're not already logged in:
   - Enter your email and password.
   - If you don’t have an account, sign up using the **Sign Up** or **Create Account** option.

3. **Access the API Keys Management Page**  
   After logging in, you’ll be redirected to the API keys management dashboard.

4. **Create a New API Key**  
   Click the **Create New API Key** or **Generate API Key** button (it’s typically easy to find).

5. **Configure Your Key**  
   You may be prompted to:
   - Give your API key a **name**.
   - Choose the **permissions/scopes**.
   - Define any **usage limits or restrictions**.

6. **Generate the Key**  
   Confirm your settings by clicking **Create** or **Generate**.

7. **Save the API Key**  
   The new API key will be shown on screen.  
   ⚠️ **Important:** Copy and securely save the key immediately. It may only be shown once.

8. **Verify Key Creation**  
   Your key should now appear in your list of active API keys on the page.

9. **Use the API Key**  
   Include it in your API requests as per the [Firecrawl documentation](https://www.firecrawl.dev/docs).

---

## 🔒 Security Notice

> Always keep your API key secure.  
> **Never** commit it to public repositories or share it publicly
