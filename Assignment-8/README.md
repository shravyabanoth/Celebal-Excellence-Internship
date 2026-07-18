# Single Agent Pipeline — Smart Assistant

A single-agent system implemented in Python that interprets a user query, routes it to the appropriate tool based on intent, executes that tool, and returns a structured response. Built as part of the Week 8 assignment on single-agent systems and agent pipelines.

## Overview

The assistant supports three categories of queries:

- **Mathematical calculations**, handled by a Calculator tool
- **Keyword extraction**, handled by a Keyword Extractor tool
- **General queries**, handled by a fallback response

Routing between these paths is determined by rule-based conditional logic applied to the incoming query.

## Project Structure

```
.
├── Week8_Sravya.ipynb   Main notebook (implementation, tests, interactive mode)
└── README.md            Project documentation
```

The notebook is organized as follows:

| Step | Description |
|------|-------------|
| 1 | Calculator tool implementation |
| 2 | Keyword Extractor tool implementation |
| 3 | Agent logic — conditional routing, logging, error handling |
| 4 | Test cases |
| 5 | Interactive mode |

## Design

### Tools

**Calculator**
Evaluates a mathematical expression and returns the result as a string. Returns `"Error in calculation"` if evaluation fails.

**Keyword Extractor**
Extracts up to five keywords (words longer than four characters) from a block of text.

### Routing Logic

| Condition | Routed to | Response type |
|---|---|---|
| Query contains `"calculate"` | Calculator tool | `calculation` |
| Query contains `"keywords"` | Keyword Extractor tool | `keywords` |
| Neither condition met | Fallback response | `general` |
| Unhandled exception during processing | — | `error` |

### Output Format

Every call to the agent returns a response in the following structure:

```json
{
  "type": "calculation | keywords | general | error",
  "result": "..."
}
```

### Error Handling and Logging

The agent wraps all routing and tool execution in a `try/except` block, so unexpected failures return a structured `error` response rather than raising an exception. Each routing decision is also logged to the console for basic traceability during execution.

## Usage

1. Open `Week8_Sravya.ipynb` in Google Colab.
2. Run all cells in order (**Runtime → Run all**).
3. In the interactive mode cell, enter a query when prompted, for example:
   - `calculate 20 + 5`
   - `extract keywords from artificial intelligence is transforming industries`
   - `what is the capital of France`
4. Enter `exit` to terminate the interactive session.

## Example

**Input**
```
calculate 20 + 5
```

**Output**
```json
{"type": "calculation", "result": "25"}
```

## Requirements

- Python 3
- Standard library only — no external dependencies

## Possible Extensions

- Additional tools (e.g., unit conversion, date/time queries)
- Intent detection based on NLP rather than keyword matching
- Persistent logging to file
- Automated unit tests for each tool and routing branch
