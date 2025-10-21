# Optimising Dolphin 3

This guide explains how to create and run an optimised version of the Dolphin 3 model using Ollama.

## Setup Commands

```bash
# Create optimised model
ollama create dolphin-optimised

# Run server with optimisations
OLLAMA_FLASH_ATTENTION=true OLLAMA_KV_CACHE_TYPE=f16 ollama serve

# Run the optimised model
ollama run --verbose dolphin-optimised:latest

# Or with OpenWebUI (Ensure Docker is running)
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

## Notes

- For more system prompts - [https://github.com/cognitivecomputations/dolphin-system-messages]
- For parameter settings - [https://github.com/ollama/ollama/blob/main/docs/modelfile.md]
- Uses Flash Attention for better performance
- Employs F16 KV cache type
- Requires Ollama to be installed
