
## Ollama Runners

3060 GPU (on proxmox)

```bash
curl http://192.168.1.49:11434/api/generate \
  -H "Content-Type: application/json" \
  -d '{
    "model": "llama3.1:8b",
    "prompt": "Say hello",
    "stream": false
  }'
```

3090 GPU (workstation)

```bash
curl http://192.168.1.34:11434/api/generate \
  -H "Content-Type: application/json" \
  -d '{
    "model": "llama3.1:8b",
    "prompt": "Say hello",
    "stream": false
  }'
```

Config
```bash
sudo systemctl edit ollama

# Current Settings
[Service]
Environment="OLLAMA_HOST=0.0.0.0"
Environment="OLLAMA_MODELS=/mnt/ai/ollama/models"
Environment="OLLAMA_NUM_GPU=999"
Environment="CUDA_VISIBLE_DEVICES=0"
Environment="OLLAMA_MODELS=/mnt/ai/ollama/models"
Environment="OLLAMA_NEW_ENGINE=1"
# Don't keep model loaded in vram / mem
Environment="OLLAMA_KEEP_ALIVE=60s"
```

## OpenClaw
view log
```bash
reset && tail -f /tmp/openclaw/openclaw-*.log
```


