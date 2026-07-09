# UnoRouter Dify Plugin

Model provider plugin that connects Dify to [UnoRouter](https://unorouter.com), an open-source OpenAI-compatible gateway serving 200+ models (Claude, GPT, Gemini, DeepSeek, Kimi, GLM, Qwen and more) behind a single API key. Models with a `:free` suffix cost nothing.

## Setup

1. Sign up at [unorouter.com](https://unorouter.com) (Discord or GitHub, no card required) and create an API key on the [token page](https://unorouter.com/token).
2. In Dify, go to Settings, then Model Provider, find UnoRouter and enter the key.
3. Pick one of the predefined models, or add any model ID from the [live catalog](https://unorouter.com/models) as a custom model.

## Predefined models

Free tier: `deepseek-v4-flash:free`, `deepseek-v4-pro:free`, `glm-5.2:free`, `qwen3.5-397b-a17b:free`, `nemotron-3-ultra-550b-a55b:free`

Paid: `claude-sonnet-5`, `gpt-5.5`, `gemini-3.5-flash`, `kimi-k2.6`, `minimax-m2.7`

Free models run on shared pools with a light per-model rate limit (about 1 request per minute per model); rotate between free models or use paid models for higher throughput.

## Development

```bash
pip install dify-plugin
python -m main
```

Package with the [dify plugin CLI](https://github.com/langgenius/dify-plugin-daemon):

```bash
dify-plugin plugin package ./
```
