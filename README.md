<p align="center">
  <img src="./assets/mesh-llm-logo.png" alt="Mesh LLM logo" width="560" />
</p>

# Mesh LLM

**mesh-llm turns spare compute into a peer-to-peer inference cloud for open models.**

mesh-llm pools GPUs across macOS and Linux machines so teams, researchers, and agents can run local or open-weight models through one OpenAI-compatible endpoint. It can serve a model on one node, distribute large models across nearby peers, route requests to specialized models, and let agents coordinate through mesh gossip.

> Work in progress — use with caution.

## What it is for

- Share spare GPU capacity across trusted machines.
- Run open models locally without a centralized inference provider.
- Serve an OpenAI-compatible API at `http://localhost:9337/v1`.
- Route requests across multiple nodes, models, and capabilities.
- Experiment with distributed inference, MoE expert sharding, and agent collaboration.

## Quick start

```bash
curl -fsSL https://github.com/Mesh-LLM/mesh-llm/releases/latest/download/mesh-bundle.tar.gz | tar xz \
  && mkdir -p ~/.local/bin \
  && mv mesh-bundle/* ~/.local/bin/
```

Join the public mesh:

```bash
mesh-llm --auto
```

Or start your own mesh with a model:

```bash
mesh-llm --model GLM-4.7-Flash
```

## Learn more

- Documentation: <https://docs.anarchai.org/>
- GitHub: <https://github.com/Mesh-LLM/mesh-llm>
- Roadmap: <https://github.com/Mesh-LLM/mesh-llm/blob/main/ROADMAP.md>
- License: MIT

Built with Rust, iroh, and llama.cpp.
