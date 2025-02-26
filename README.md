# Finetuning Dolphin 3

This guide explains how to create and run an optimized version of the Dolphin 3 model using Ollama.

## Setup Commands

```bash
# Create optimized model
ollama create dolphin-optimised

# Run server with optimizations
OLLAMA_FLASH_ATTENTION=true OLLAMA_KV_CACHE_TYPE=f16 ollama serve

# Run the optimized model
ollama run dolphin-optimised:latest
```

## Notes

- Uses Flash Attention for better performance
- Employs F16 KV cache type
- Requires Ollama to be installed
