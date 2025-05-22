# arXiv Research Chatbot with MCP Integration

A Python-based chatbot that helps users search and retrieve information from arXiv papers using natural language queries. The chatbot uses the Claude API for natural language processing, the arXiv API for paper searches, and integrates with the Model Context Protocol (MCP) for enhanced functionality.

## Features

- Search for papers on arXiv based on topics
- Store paper information (title, authors, summary, URL, publication date)
- Retrieve information about specific papers
- Interactive chat interface
- Organized storage of paper information by topics
- MCP integration for enhanced context and research capabilities

## Prerequisites

- Python 3.11 or higher
- Anthropic API key (for Claude API access)
- Node.js and npm (for MCP filesystem server)
- UV package manager (for Python dependencies)

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd <repository-name>
```

2. Install the required packages:

```bash
uv pip install -r requirements.txt
```

3. Create a `.env` file in the project root directory and add your Anthropic API key:

```
anthropic_key=your_api_key_here
```

4. Install MCP dependencies:

```bash
npm install -g @modelcontextprotocol/server-filesystem
```

## Project Structure

- `MCP_project/`: Main project directory
  - `research_server.py`: MCP research server implementation
  - `papers/`: Directory where paper information is stored
    - Organized by topics in subdirectories
    - Each topic directory contains a `papers_info.json` file
- `requirements.txt`: Python package dependencies
- `claude_desktop_config.json`: MCP server configuration

## MCP Server Configuration

The project uses three MCP servers:

1. Filesystem Server: Manages file system operations
2. Research Server: Handles research-related queries and operations
3. Fetch Server: Manages data fetching operations

## Usage

1. Start the MCP servers:

```bash
# Start the research server
uv run research_server.py

# Start the filesystem server
npx @modelcontextprotocol/server-filesystem
```

2. Open the chat interface and start interacting with the chatbot. Example queries:
   - "Search for 2 papers on LLM interpretability"
   - "Find information about paper 1310.7911v2"

## Available Tools

1. `search_papers`: Searches for papers on arXiv based on a topic

   - Parameters:
     - `topic`: The topic to search for
     - `max_results`: Maximum number of results (default: 5)

2. `extract_info`: Retrieves information about a specific paper
   - Parameters:
     - `paper_id`: The ID of the paper to look for

## Notes

- The chatbot integrates with MCP for enhanced context awareness
- Paper information is stored locally in JSON files
- The `papers` directory is automatically created when searching for papers

## Resources

- [Anthropic API Documentation](https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview#how-to-implement-tool-use)
- [arXiv API Documentation](https://arxiv.org/help/api/)
- [Model Context Protocol Documentation](https://github.com/anthropics/model-context-protocol)
