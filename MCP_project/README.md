# MCP Research Server Implementation

This directory contains the implementation of the Model Context Protocol (MCP) research server for the arXiv Research Chatbot. The server enhances the chatbot's capabilities by providing structured access to research-related operations and data.

## Components

### Research Server (`research_server.py`)

The main MCP server implementation that handles research-related queries and operations. This server:

- Processes research queries
- Manages paper searches and information retrieval
- Integrates with the arXiv API
- Maintains local paper storage

### Papers Directory

- Stores paper information organized by topics
- Each topic has its own subdirectory
- Papers are stored in JSON format for easy access and updates

## Setup

1. Ensure you have the required dependencies:

```bash
uv pip install -r requirements.txt
```

2. Configure the server:

- The server is configured through `claude_desktop_config.json` in the parent directory
- Make sure the paths in the configuration match your setup

## Running the Server

Start the research server using:

```bash
uv run research_server.py
```

The server will start and be ready to handle research-related queries from the main chatbot.

## Integration

This server works in conjunction with two other MCP servers:

1. Filesystem Server: Handles file operations
2. Fetch Server: Manages data fetching

## Development

When making changes to the research server:

1. Update the server implementation in `research_server.py`
2. Test the changes locally
3. Update the configuration if necessary
4. Document any new features or changes

## Error Handling

The server includes error handling for:

- API connection issues
- Invalid queries
- File system operations
- Data parsing errors

## Contributing

When contributing to this project:

1. Follow the existing code structure
2. Add appropriate error handling
3. Update documentation for new features
4. Test changes thoroughly before committing

## Resources

- [Model Context Protocol Documentation](https://github.com/anthropics/model-context-protocol)
- [arXiv API Documentation](https://arxiv.org/help/api/)
