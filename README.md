# arXiv Research Chatbot

A Python-based chatbot that helps users search and retrieve information from arXiv papers using natural language queries. The chatbot uses the Claude API for natural language processing and the arXiv API for paper searches.

## Features

- Search for papers on arXiv based on topics
- Store paper information (title, authors, summary, URL, publication date)
- Retrieve information about specific papers
- Interactive chat interface
- Organized storage of paper information by topics

## Prerequisites

- Python 3.11 or higher
- Anthropic API key (for Claude API access)

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd <repository-name>
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root directory and add your Anthropic API key:

```
anthropic_key=your_api_key_here
```

## Project Structure

- `chatBot.ipynb`: Main Jupyter notebook containing the chatbot implementation
- `papers/`: Directory where paper information is stored
  - Organized by topics in subdirectories
  - Each topic directory contains a `papers_info.json` file
- `requirements.txt`: Python package dependencies

## Usage

1. Open the `chatBot.ipynb` notebook in Jupyter:

```bash
jupyter notebook chatBot.ipynb
```

2. Run all cells in the notebook

3. Start interacting with the chatbot. Example queries:
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

- The chatbot doesn't persist memory across queries
- Paper information is stored locally in JSON files
- The `papers` directory is automatically created when searching for papers

## Resources

- [Anthropic API Documentation](https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview#how-to-implement-tool-use)
- [arXiv API Documentation](https://arxiv.org/help/api/)
