# N8N
Teste do N8N com as integrações do Telegram, Whatsapp.

## Testes
 * Telegram
 * Whatsapp com o Waha
 * AI Agent com o Ollama local usando deepseek-r1:8b

### verificando load da GPU nVidia em notebooks
```bash
# para não receber o erro "This version of Nvtop is missing support for reporting Intel GPU memory, power, fan and temperature"
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia nvtop

__NV_PRIME_RENDER_OFFLOAD=0 __GLX_VENDOR_LIBRARY_NAME=nvidia nvtop
```

### Ollama usando GPU
```bash
# dá documentação oficial Ollama docker
docker run -d --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

#### Links
 * [ollama docker](https://ollama.com/blog/ollama-is-now-available-as-an-official-docker-image)