# Full Stack AI Agent Template - Customization Guide

## Architecture
```
React Frontend --> FastAPI/Express --> AI Agent --> LLM Provider
     |                 |                |
  Chat UI          WebSocket        Tool Use
  History          Auth/Session     Memory/RAG
```

## Supported LLM Providers
| Provider | Models | Setup |
|----------|--------|-------|
| OpenAI | GPT-4, GPT-3.5 | API key |
| Anthropic | Claude 3.5 | API key |
| Local | Ollama, vLLM | Self-hosted |

## Adding Custom Tools
```python
@tool
def my_tool(query: str) -> str:
    """Description of what this tool does."""
    return process(query)
```

## Configuration
| Variable | Description |
|----------|-------------|
| LLM_PROVIDER | openai, anthropic, local |
| MODEL_NAME | Model identifier |
| TEMPERATURE | Response creativity (0-1) |
| MAX_TOKENS | Max response length |

## Quick Start
```bash
git clone https://github.com/MaxCode0917/full-stack-ai-agent-template.git
cp .env.example .env
docker-compose up
```