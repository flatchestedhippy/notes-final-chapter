
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
