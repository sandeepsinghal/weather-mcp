https://modelcontextprotocol.io/quickstart/server

# Create a new directory for our project
uv init weather
cd weather

# Create virtual environment and activate it
uv venv
source .venv/bin/activate

# Install dependencies
uv add "mcp[cli]" httpx

# Create and run our server file
touch weather.py
enter code 
uv run weather.py 

# Modify claude config 
vi ~/Library/Application\ Support/Claude/claude_desktop_config.json

# Add MCP server config 

{
  "mcpServers": {
    "weather": {
      "command": "/Users/ssinghal/.local/bin/uv",
      "args": [
        "--directory",
        "/Users/Shared/u001/src/github/ai-learn/weather-mcp",
        "run",
        "weather.py"
      ]
    }
  }
}

