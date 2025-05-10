# Fake News Detection Multi-Agent System

This project implements a multi-agent system for detecting fake news using a combination of AI techniques. The system consists of three main agents:

1. **Orchestrator Agent**: Coordinates the overall process and manages communication between agents.
2. **Search Agent**: Searches through historical news articles to find relevant information for fact-checking using Google Search MCP Server.
3. **Scorer Agent**: Analyzes news content and determines its authenticity based on various factors using Google's Gemini API.

## Setup

1. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

2. Create a `.env` file in the root directory with your API keys:
   ```
   GOOGLE_API_KEY=your_google_api_key
   MCP_SERVER_URL=http://localhost:3000  # URL for the Google Search MCP Server
   ```

3. Set up the Google Search MCP Server:
   - Clone the repository: `git clone https://github.com/mixelpixx/Google-Search-MCP-Server.git`
   - Follow the installation instructions in the repository
   - Configure your Google API credentials and Custom Search Engine ID
   - Start the MCP server

3. Run the system:
   ```
   python main.py
   ```

## Usage

The system takes a news article or claim as input and returns an authenticity score along with supporting evidence.

## Project Structure

- `main.py`: Entry point for the application
- `agents/`: Contains the implementation of all agents
  - `orchestrator.py`: Orchestrator agent implementation
  - `search_agent.py`: Search agent for historical news lookup
  - `scorer_agent.py`: Scorer agent for authenticity detection
- `utils/`: Utility functions and helpers
